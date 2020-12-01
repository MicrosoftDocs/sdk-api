---
UID: NF:tom.ITextRange.Paste
title: ITextRange::Paste (tom.h)
description: Pastes text from a specified data object.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","Paste method","ITextRange.Paste","ITextRange::Paste","Paste","Paste method [Windows Controls]","Paste method [Windows Controls]","ITextRange interface","_win32_ITextRange_Paste","_win32_ITextRange_Paste_cpp","controls.ITextRange_Paste","controls._win32_ITextRange_Paste","tom/ITextRange::Paste"]
old-location: controls\ITextRange_Paste.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\paste.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],Paste method, ITextRange.Paste, ITextRange::Paste, Paste, Paste method [Windows Controls], Paste method [Windows Controls],ITextRange interface, _win32_ITextRange_Paste, _win32_ITextRange_Paste_cpp, controls.ITextRange_Paste, controls._win32_ITextRange_Paste, tom/ITextRange::Paste
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
 - ITextRange::Paste
 - tom/ITextRange::Paste
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
 - ITextRange.Paste
---

# ITextRange::Paste


## -description

Pastes text from a specified data object.

## -parameters

### -param pVar

Type: <b>VARIANT*</b>

The <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> to paste. However, the contents of the clipboard are used if any of the following are true.
                

<i>pVar</i> is null 

<i>pVar</i> punkVal is null 

<i>pVar</i> is not <b>VT_UNKNOWN</b>

<i>pVar</i> punkVal does not return an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> when queried for one

### -param Format

Type: <b>long</b>

The clipboard format to use in the paste operation. Zero is best format, which usually is RTF, but <b>CF_UNICODETEXT</b> and other formats are also possible. The default value is zero. For more information, see <a href="/windows/desktop/dataxchg/clipboard-formats">Clipboard Formats</a>.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Destination is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Destination cannot contain the text to be pasted.

</td>
</tr>
</table>

## -remarks

For more information, see<a href="/windows/desktop/api/tom/nf-tom-itextrange-copy">ITextRange::Copy</a>.

## -see-also

<a href="/windows/desktop/dataxchg/clipboard-formats">Clipboard Formats</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-copy">Copy</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>