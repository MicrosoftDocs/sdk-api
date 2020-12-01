---
UID: NF:tom.ITextDocument.Save
title: ITextDocument::Save (tom.h)
description: Saves the document.
helpviewer_keywords: ["ITextDocument interface [Windows Controls]","Save method","ITextDocument.Save","ITextDocument::Save","Save","Save method [Windows Controls]","Save method [Windows Controls]","ITextDocument interface","_win32_ITextDocument_Save","_win32_ITextDocument_Save_cpp","controls.ITextDocument_Save","controls._win32_ITextDocument_Save","tom/ITextDocument::Save"]
old-location: controls\ITextDocument_Save.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\save.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],Save method, ITextDocument.Save, ITextDocument::Save, Save, Save method [Windows Controls], Save method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Save, _win32_ITextDocument_Save_cpp, controls.ITextDocument_Save, controls._win32_ITextDocument_Save, tom/ITextDocument::Save
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
 - ITextDocument::Save
 - tom/ITextDocument::Save
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
 - ITextDocument.Save
---

# ITextDocument::Save


## -description

Saves the document.

## -parameters

### -param pVar [in]

Type: <b>VARIANT*</b>

The save target. This parameter is a <b>VARIANT</b>, which can be a file name, or <b>NULL</b>.

### -param Flags [in]

Type: <b>long</b>

File creation, open, share, and conversion flags. For a list of possible values, see <a href="/windows/desktop/api/tom/nf-tom-itextdocument-open">ITextDocument::Open</a>.

### -param CodePage [in]

Type: <b>long</b>

The specified code page. Common values are CP_ACP (zero: system ANSI code page), 1200 (Unicode), and 1208 (UTF-8).

## -returns

Type: <b>HRESULT</b>

The return value can be an 
						<b>HRESULT</b> value that corresponds to a system error code or a COM error code, including one of the following values.

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
Method succeeds.

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

To use the parameters that were specified for opening the file, use zero values for the parameters. 

If 
				<i>pVar</i> is null or missing, the file name given by this document's name is used. If both of these are missing or null, the method fails. 

If 
				<i>pVar</i> specifies a file name, that name should replace the current Name property. Similarly, the 
				<i>Flags</i> and 
				<i>CodePage</i> arguments can overrule those supplied in the 
				<a href="/windows/desktop/api/tom/nf-tom-itextdocument-open">ITextDocument::Open</a> method and define the values to use for files created with the 
				<a href="/windows/desktop/api/tom/nf-tom-itextdocument-new">ITextDocument::New</a> method.

Unicode plain-text files should be saved with the Unicode byte-order mark (0xFEFF) as the first character. This character should be removed when the file is read in; that is, it is only used for import/export to identify the plain text as Unicode and to identify the byte order of that text. Microsoft Notepad adopted this convention, which is now recommended by the Unicode standard.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-new">New</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-open">Open</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>