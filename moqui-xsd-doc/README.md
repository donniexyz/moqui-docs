# Moqui XSD Schema Documentations

This document is generated from moqui's XSD files with help of xs3p an xslt stylesheet.


# How to generate Moqui XSD documentation

## Summary
To generate human friendly html documentation from moqui XSD files, you can use xs3p which is a xslt stylesheet. To use xs3p you need XSLT processor, for example: msxsl (windows), xalan (java), or xsltproc (linux).

### tools:
    msxsl.exe (get it from https://www.microsoft.com/en-us/download/details.aspx?id=21714)
    xs3p      (get it from http://xml.fiforms.org/xs3p/)
    
#### example:
    r:\>msxsl xml-form-1.5.xsd b:xs3p.xsl -o r:\xml-form-1.5.html -v -t
    Microsoft (R) XSLT Processor Version 4.0
    
    Source document load time:     5.512 milliseconds
    Stylesheet document load time: 21.63 milliseconds
    Stylesheet compile time:       16.56 milliseconds
    Stylesheet execution time:     70.84 milliseconds
    
    r:\>
    
### result:
    file form.html can be read by normal browser.


For your convinience the xsd documentation has been generated and can be found here.

    
To generate all xsd file:
    
    > cd %moqui_root%\framework\xsd

    > for %f in (*.xsd) do msxsl %f r:\xs3p.xsl -o r:\moqui-doc-xsd\%~nf.html -v -t title="XML Schema Document: %f"
    
    
