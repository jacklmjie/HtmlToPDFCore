[![Nuget count](http://img.shields.io/nuget/v/HtmlToPDFCore.svg)](http://www.nuget.org/packages/HtmlToPDFCore/)
[![.NET Core](https://github.com/carloscds/HtmlToPDFCore/workflows/.NET%20Core/badge.svg)](https://github.com/carloscds/HtmlToPDFCore/actions)

[linux wkhtmltopdf 运行报错](https://blog.csdn.net/u014028634/article/details/80902702)

# HtmlToPDFCore
Convert HTML to PDF

This package is huge because include Rotativa files for Windows, Linux and MAC. 

Using this tool you can convert an HTML file to PDF file.

### How to use
```csharp
static void Main(string[] args)
{
    var html = @"
        <html>
            <title>PDF</title>
            <body>
                <b>PDF Sample - Carlos dos Santos</b>
            </body>
        </html>";

    var htmlToPdf = new HtmlToPDFCore.HtmlToPDF();
    var pdf = htmlToPdf.ReturnPDF(html);

    FileStream fs = new FileStream("teste.pdf",FileMode.CreateNew);
    fs.Write(pdf,0,pdf.Length);
    fs.Close();
}
```

### Environment Tested

Windows
Linux
Microsoft Azure AppServices using Linux Service Plan

### Contributing

Feel free to use and contribute with this project.
