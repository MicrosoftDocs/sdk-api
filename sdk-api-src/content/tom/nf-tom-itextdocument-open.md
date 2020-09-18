---
UID: NF:tom.ITextDocument.Open
title: ITextDocument::Open (tom.h)
description: Opens a specified document. There are parameters to specify access and sharing privileges, creation and conversion of the file, as well as the code page for the file.
helpviewer_keywords: ["ITextDocument interface [Windows Controls]","Open method","ITextDocument.Open","ITextDocument::Open","Open","Open method [Windows Controls]","Open method [Windows Controls]","ITextDocument interface","_win32_ITextDocument_Open","_win32_ITextDocument_Open_cpp","controls.ITextDocument_Open","controls._win32_ITextDocument_Open","tom/ITextDocument::Open","tomCreateAlways","tomCreateNew","tomHTML","tomOpenAlways","tomOpenExisting","tomPasteFile","tomRTF","tomReadOnly","tomShareDenyRead","tomShareDenyWrite","tomText","tomTruncateExisting","tomWordDocument"]
old-location: controls\ITextDocument_Open.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\open.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],Open method, ITextDocument.Open, ITextDocument::Open, Open, Open method [Windows Controls], Open method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Open, _win32_ITextDocument_Open_cpp, controls.ITextDocument_Open, controls._win32_ITextDocument_Open, tom/ITextDocument::Open, tomCreateAlways, tomCreateNew, tomHTML, tomOpenAlways, tomOpenExisting, tomPasteFile, tomRTF, tomReadOnly, tomShareDenyRead, tomShareDenyWrite, tomText, tomTruncateExisting, tomWordDocument
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextDocument::Open
 - tom/ITextDocument::Open
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextDocument.Open
---

# ITextDocument::Open


## -description

Opens a specified document. There are parameters to specify access and sharing privileges, creation and conversion of the file, as well as the code page for the file.

## -parameters

### -param pVar [in]

Type: <b>VARIANT*</b>

A <b>VARIANT</b> that specifies the name of the file to open.

### -param Flags

Type: <b>long</b>

The file creation, open, share, and conversion flags. Default value is zero, which gives read/write access and read/write sharing, open always, and automatic recognition of the file format (unrecognized file formats are treated as text). Other values are defined in the following groups.


Any combination of these values may be used.



<a id="tomReadOnly"></a>
<a id="tomreadonly"></a>
<a id="TOMREADONLY"></a>


#### tomReadOnly

<a id="tomShareDenyRead"></a>
<a id="tomsharedenyread"></a>
<a id="TOMSHAREDENYREAD"></a>


#### tomShareDenyRead

<a id="tomShareDenyWrite"></a>
<a id="tomsharedenywrite"></a>
<a id="TOMSHAREDENYWRITE"></a>


#### tomShareDenyWrite

<a id="tomPasteFile"></a>
<a id="tompastefile"></a>
<a id="TOMPASTEFILE"></a>


#### tomPasteFile


These values are mutually exclusive.



<a id="tomCreateNew"></a>
<a id="tomcreatenew"></a>
<a id="TOMCREATENEW"></a>


#### tomCreateNew

<a id="tomCreateAlways"></a>
<a id="tomcreatealways"></a>
<a id="TOMCREATEALWAYS"></a>


#### tomCreateAlways

<a id="tomOpenExisting"></a>
<a id="tomopenexisting"></a>
<a id="TOMOPENEXISTING"></a>


#### tomOpenExisting

<a id="tomOpenAlways"></a>
<a id="tomopenalways"></a>
<a id="TOMOPENALWAYS"></a>


#### tomOpenAlways

<a id="tomTruncateExisting"></a>
<a id="tomtruncateexisting"></a>
<a id="TOMTRUNCATEEXISTING"></a>


#### tomTruncateExisting

<a id="tomRTF"></a>
<a id="tomrtf"></a>
<a id="TOMRTF"></a>


#### tomRTF

<a id="tomText"></a>
<a id="tomtext"></a>
<a id="TOMTEXT"></a>


#### tomText

<a id="tomHTML"></a>
<a id="tomhtml"></a>
<a id="TOMHTML"></a>


#### tomHTML

<a id="tomWordDocument"></a>
<a id="tomworddocument"></a>
<a id="TOMWORDDOCUMENT"></a>


#### tomWordDocument

### -param CodePage

Type: <b>long</b>

The code page to use for the file. Zero (the default value) means <b>CP_ACP</b> (ANSI code page) unless the file begins with a Unicode BOM 0xfeff, in which case the file is considered to be Unicode. Note that code page 1200 is Unicode, <b>CP_UTF8</b> is UTF-8.

## -returns

Type: <b>HRESULT</b>

The return value can be an <b>HRESULT</b> value that corresponds to a system error or COM error code, including one of the following values. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeds

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Feature not implemented.

</td>
</tr>
</table>

## -remarks

If a document is created with the <a href="/windows/desktop/api/tom/nf-tom-itextdocument-new">ITextDocument::New</a> method and the zero values are used, then the Text Object Model (TOM) engine has to choose which flags and code page to use. UTF-8 Rich Text Format (RTF) (defined below) is an attractive default.

Microsoft Rich Edit 3.0 defines a control word, \urtf8, which should be used instead of \rtf1. This means the file is encoded in UTF-8. On input, RTF files contain the relevant code-page information, but this can be changed for saving purposes, thereby allowing one version to be translated to another.

If the tomPasteFile flag is not set in the <i>Flags</i> parameter, the method first closes the current document after saving any unsaved changes.

A file is recognized as a Unicode text file if it starts with the Unicode BOM 0xfeff. The <b>ITextDocument::Open</b> method strips off this Unicode BOM on input and <a href="/windows/desktop/api/tom/nf-tom-itextdocument-save">ITextDocument::Save</a> applies it on output. See the comments on the <b>ITextDocument::Save</b> method, which discuss putting the Unicode BOM at the beginning of Unicode plain-text files. The conversion values <b>tomRTF</b>, <b>tomHTML</b>, and <b>tomWordDocument</b> are used primarily for the <b>ITextDocument::Save</b> method, since these formats are easily recognized on input. 

Errors are reported by negative values, but because file operations have many kinds of errors, you may not need all of the error information provided. In particular, you may not care (or you may already know) which file facility is used, namely Windows (<code>pVar.vt = VT_BSTR</code>) or OLE storage for <a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>. By masking off bit 18 of an <b>HRESULT</b> value, you can ignore the difference and compare to its <b>STG_E_xxx</b> value. For example:




```
HRESULT hr;
VARIANT Var;
VariantInit(&Var)

Var.vt = VT_BSTR;
Var.bstrVal = SysAllocString(L"test.txt"); // Use file command
hr = pDoc->Open(&Var, tomOpenExisting, 0);
hr &= ~0x40000; // Mask off bit 18
if(hr == STG_E_FILENOTFOUND)
{
...// the rest of the code
}
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-save">Save</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>