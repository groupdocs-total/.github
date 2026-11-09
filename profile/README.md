<h1 align="center">GroupDocs.Total</h1>

<h3 align="center">Every GroupDocs Document API in One Package for .NET, Java, Node.js and Python</h3>

<p align="center">
  <strong>GroupDocs.Total</strong> puts the 14 GroupDocs document APIs into one package per platform: view, convert, compare, annotate, sign and edit documents, merge and split them, add and remove watermarks, redact sensitive content, read and remove metadata, extract text, tables and images, index and search document collections, generate reports from templates, and export documents to Markdown. 200+ file formats, one license, on-premise SDKs for .NET, Java, Node.js and Python, and an MCP server for AI agents.
</p>

[![Product Page](https://img.shields.io/badge/Product%20Page-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.com/total/)
[![Docs](https://img.shields.io/badge/Docs-2865E0?style=for-the-badge&logo=Hugo&logoColor=white)](https://docs.groupdocs.com/total/)
[![Demos](https://img.shields.io/badge/Demos-2865E0?style=for-the-badge&logo=appveyor&logoColor=white)](https://products.groupdocs.app/total)
[![Blog](https://img.shields.io/badge/Blog-2865E0?style=for-the-badge&logo=WordPress&logoColor=white)](https://blog.groupdocs.com/category/total/)
[![Search](https://img.shields.io/badge/Search-2865E0?style=for-the-badge&logo=searchengin&logoColor=white)](https://search.groupdocs.com/)
[![Support](https://img.shields.io/badge/Support-2865E0?style=for-the-badge&logo=Discourse&logoColor=white)](https://forum.groupdocs.com/c/total)
[![Temp License](https://img.shields.io/badge/Temp%20License-2865E0?style=for-the-badge&logo=rocket&logoColor=white)](https://purchase.groupdocs.com/temporary-license)

## Latest Total News & Updates
* **NEW:** GroupDocs.Total for Python via .NET 26.11.0: `pip install groupdocs-total-net` installs 14 products, now with Parser, Search, Annotation, Editor and Markdown, on Python 3.5 - 3.14 for Windows, Linux and macOS. [PyPI](https://pypi.org/project/groupdocs-total-net/26.11.0/) | [Release notes](https://releases.groupdocs.com/total/python-net/release-notes/2026/groupdocs-total-for-python-via-net-26-11-release-notes/)
* GroupDocs.Total for Java 26.10 and for Node.js via Java 26.10: Comparison 26.10 compares PDFs side by side, Conversion 26.9 can cancel long conversions, Viewer 26.9 renders OFD, Search 26.9.1 brings a new index format that existing indexes upgrade to in place, and Assembly 26.10.1 joins the Node.js package. [Java release notes](https://releases.groupdocs.com/total/java/release-notes/2026/groupdocs-total-for-java-26-10-release-notes/) | [Node.js release notes](https://releases.groupdocs.com/total/nodejs-java/release-notes/2026/groupdocs-total-for-node-js-via-java-26-10-release-notes/)
* Published [GroupDocs.Total 26.6](https://www.nuget.org/packages/GroupDocs.Total/) for .NET on NuGet: it drops its dependency on the `Aspose.Drawing` package, keeps MSG properties and headers after a Metadata save, and fixes Viewer rendering of PNG, JPG and PPTX on Linux. [Release notes](https://releases.groupdocs.com/total/net/release-notes/2026/groupdocs-total-for-net-26-6-release-notes/)
* [GroupDocs.Total.Mcp](https://github.com/groupdocs-total/GroupDocs.Total.Mcp) 26.7.3: one MCP server with 38 document tools, published as a Docker image and listed in the MCP Registry.

## Supported Platforms & Repository Groups

### .NET Document Processing (C#, ASP.NET, Services)
One NuGet package with the 14 GroupDocs APIs for .NET 6 and later.
* **[GroupDocs.Total-for-.NET](https://github.com/groupdocs-total/GroupDocs.Total-for-.NET)**: A console example per feature for every product, and two complete ASP.NET web applications.

```csharp
using GroupDocs.Conversion;
using GroupDocs.Conversion.Options.Convert;
using GroupDocs.Watermark;
using GroupDocs.Watermark.Watermarks;
using Font = GroupDocs.Watermark.Watermarks.Font;

// Convert a Word document to PDF, then watermark the PDF
using (var converter = new Converter("document.docx"))
{
    converter.Convert("document.pdf", new PdfConvertOptions());
}
using (var watermarker = new Watermarker("document.pdf"))
{
    watermarker.Add(new TextWatermark("CONFIDENTIAL", new Font("Arial", 36)));
    watermarker.Save("watermarked.pdf");
}
```

### Java Document Processing (Maven, Spring)
One Maven artifact with the 14 GroupDocs APIs for Java.
* **[GroupDocs.Total-for-Java](https://github.com/groupdocs-total/GroupDocs.Total-for-Java)**: A self-contained class per feature for every product; the package `com.groupdocs:groupdocs-total` comes from the [GroupDocs Maven repository](https://releases.groupdocs.com/java/repo/).

```java
import com.groupdocs.conversion.Converter;
import com.groupdocs.conversion.options.convert.PdfConvertOptions;
import com.groupdocs.watermark.Watermarker;
import com.groupdocs.watermark.watermarks.Font;
import com.groupdocs.watermark.watermarks.TextWatermark;

// Convert a Word document to PDF, then watermark the PDF
try (Converter converter = new Converter("document.docx")) {
    converter.convert("document.pdf", new PdfConvertOptions());
}
try (Watermarker watermarker = new Watermarker("document.pdf")) {
    watermarker.add(new TextWatermark("CONFIDENTIAL", new Font("Arial", 36)));
    watermarker.save("watermarked.pdf");
}
```

### Node.js Document Processing (Node.js via Java)
The Java suite in Node.js: `npm install @groupdocs/groupdocs.total`, with Java 8 or later on `PATH`.
* **[GroupDocs.Total-for-Node.js-via-Java](https://github.com/groupdocs-total/GroupDocs.Total-for-Node.js-via-Java)**: A script per feature across the bundled products.
* [Documentation](https://docs.groupdocs.com/total/nodejs-java/) | [Release Notes](https://releases.groupdocs.com/total/nodejs-java/release-notes/)

```javascript
const groupdocs = require('@groupdocs/groupdocs.total');
const java = require('java');
const PdfConvertOptions = java.import('com.groupdocs.conversion.options.convert.PdfConvertOptions');

// Convert a Word document to PDF
const converter = new groupdocs.Converter('document.docx');
converter.convert('document.pdf', new PdfConvertOptions());
converter.close();
```

### Python Document Processing (Python via .NET)
`pip install groupdocs-total-net` installs the 14 GroupDocs for Python via .NET packages, each with the .NET runtime embedded: Python 3.5 - 3.14 on Windows, Linux and macOS, about 2.2 GB to download.
* **[GroupDocs.Total-for-Python-via-.NET](https://github.com/groupdocs-total/GroupDocs.Total-for-Python-via-.NET)**: Links to the runnable examples of all 14 products, and how to combine products in one script.
* [PyPI](https://pypi.org/project/groupdocs-total-net/) | [Docs](https://docs.groupdocs.com/total/python-net/) | [Release Notes](https://releases.groupdocs.com/total/python-net/release-notes/)

```python
import os

os.environ["DOTNET_MULTILEVEL_LOOKUP"] = "0"  # Windows: every product keeps its own .NET runtime

from groupdocs.conversion import Converter
from groupdocs.conversion.options.convert import PdfConvertOptions
from groupdocs.watermark import Watermarker
from groupdocs.watermark.watermarks import TextWatermark, Font

# Convert a Word document to PDF, then watermark the PDF
with Converter("document.docx") as converter:
    converter.convert("document.pdf", PdfConvertOptions())

with Watermarker("document.pdf") as watermarker:
    watermarker.add(TextWatermark("CONFIDENTIAL", Font("Arial", 36.0)))
    watermarker.save("watermarked.pdf")
```

### MCP Server for AI Agents (Claude, Cursor, Copilot)
Let AI agents work with documents through the GroupDocs engines, **locally over MCP**: 38 tools for annotation, comparison, conversion, Markdown, merging, metadata, parsing, redaction, signing and watermarking, plus document info and page previews. No uploads; without a license it runs in evaluation mode.
* **[GroupDocs.Total.Mcp](https://github.com/groupdocs-total/GroupDocs.Total.Mcp)**: The MCP server (MIT), with one-click installs for VS Code and Cursor and configs for Claude Code, Codex CLI, Visual Studio 2022, Windsurf, Cline and JetBrains Rider. It ships as a Docker image only: the engines exceed NuGet's 250 MB limit.
* **[GroupDocs.Mcp.Installer](https://github.com/groupdocs/GroupDocs.Mcp.Installer)**: Cross-platform installer that registers the server with your MCP clients and verifies it.
* **[GroupDocs.Total.Mcp.Tests](https://github.com/groupdocs-total/GroupDocs.Total.Mcp.Tests)**: Integration tests for the server.

```bash
# Run the server on the documents folder, then ask your agent:
docker run --rm -i -v $(pwd)/documents:/data ghcr.io/groupdocs-total/total-net-mcp:latest
```

> "Convert contract.docx to PDF, then sign it with a QR code containing 'Signed by Alice', then watermark every page with 'CONFIDENTIAL'"
> "Compare old.pdf and new.pdf, list every annotation in the result, and preview page 1"

[Docker image](https://github.com/orgs/groupdocs-total/packages/container/package/total-net-mcp) | [MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=io.github.groupdocs-total/groupdocs-total-mcp)

## Business Use-Cases
- **Document intake pipelines:** convert incoming files to PDF, then watermark, sign and archive them in one service.
- **Review and approval:** render documents in the browser, compare versions, and collect annotations and comments.
- **Privacy and compliance:** redact personal data, remove metadata, and verify signatures before documents leave the organization.
- **Search and data extraction:** index document stores for full-text search, and extract text, tables, images and barcodes.
- **Document generation:** fill templates with data, then merge, split, convert or export the results to Markdown.

## API Key Features & Benefits
- 14 products in one package: Viewer, Conversion, Comparison, Annotation, Signature, Editor, Merger, Watermark, Redaction, Metadata, Parser, Search, Assembly and Markdown.
- 200+ file formats across the suite: Word, Excel, PowerPoint, PDF, images, email, CAD, Visio, HTML, e-books and archives.
- One license for every product on your platform, and a temporary license for full-feature evaluation.
- On-premise: documents never leave your servers, and no Microsoft Office or Adobe Acrobat is needed.
- The same load, process and save pattern in every product and on every platform.

## Getting Started
- .NET: `dotnet add package GroupDocs.Total`
- Java: add `com.groupdocs:groupdocs-total` from the GroupDocs repository, `https://releases.groupdocs.com/java/repo/`
- Node.js: `npm install @groupdocs/groupdocs.total`, with Java 8 or later on `PATH`
- Python: `pip install groupdocs-total-net`
- MCP server: `docker run --rm -i -v $(pwd)/documents:/data ghcr.io/groupdocs-total/total-net-mcp:latest`
- Run the examples from the repositories above, one per feature of every product.

## Technical Support & Resources
- Documentation and tutorials: https://docs.groupdocs.com/total/
- Releases and release notes: https://releases.groupdocs.com/total/
- Free support forum: https://forum.groupdocs.com/c/total
- Temporary license for full-feature evaluation: https://purchase.groupdocs.com/temporary-license

## Security & Legal
- Security policy: https://about.groupdocs.com/security/
- Legal: https://about.groupdocs.com/legal/

## Tags

`groupdocs-total` `document-processing` `document-api` `document-conversion` `document-viewer` `document-comparison` `document-annotation` `e-signature` `document-editor` `pdf-merge` `watermark` `redaction` `metadata` `text-extraction` `full-text-search` `document-automation` `markdown` `dotnet` `java` `nodejs` `python` `mcp` `mcp-server` `ai-agents`

---

<p align="center">
  If this ecosystem helps you, <a href="https://github.com/groupdocs-total">star</a> the repos and <a href="https://github.com/groupdocs-total?tab=followers">follow</a> the organization.
</p>
