---
UID: NF:tom.ITextRange.CanPaste
title: ITextRange::CanPaste (tom.h)
description: Determines if a data object can be pasted, using a specified format, into the current range.
helpviewer_keywords: ["CanPaste","CanPaste method [Windows Controls]","CanPaste method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","CanPaste method","ITextRange.CanPaste","ITextRange::CanPaste","_win32_ITextRange_CanPaste","_win32_ITextRange_CanPaste_cpp","controls.ITextRange_CanPaste","controls._win32_ITextRange_CanPaste","tom/ITextRange::CanPaste"]
old-location: controls\ITextRange_CanPaste.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\canpaste.htm
ms.date: 12/05/2018
ms.keywords: CanPaste, CanPaste method [Windows Controls], CanPaste method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],CanPaste method, ITextRange.CanPaste, ITextRange::CanPaste, _win32_ITextRange_CanPaste, _win32_ITextRange_CanPaste_cpp, controls.ITextRange_CanPaste, controls._win32_ITextRange_CanPaste, tom/ITextRange::CanPaste
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
 - ITextRange::CanPaste
 - tom/ITextRange::CanPaste
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
 - ITextRange.CanPaste
---

# ITextRange::CanPaste


## -description

Determines if a data object can be pasted, using a specified format, into the current range.

## -parameters

### -param pVar

Type: <b>VARIANT*</b>

The 
					<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> to be pasted. However, the Clipboard contents are checked for pasting if any of the following are true: 
					

<ul>
<li><i>pVar</i> is null </li>
<li><i>pVar</i>-&gt;punkVal is null </li>
<li><i>pVar</i>-&gt;vt is not <b>VT_UNKNOWN</b></li>
<li><i>pVar</i>-&gt;punkVal does not return an 
							<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object when queried for one </li>
</ul>

### -param Format

Type: <b>long</b>

Clipboard format that is used. Zero represents the best format, which usually is RTF, but <b>CF_UNICODETEXT</b> and other formats are also possible. The default value is zero.

### -param pValue

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that is <b>tomTrue</b> only if the data object identified by 
					<i>pVar</i> can be pasted, using the specified format, into the range. This parameter can null.

## -returns

Type: <b>HRESULT</b>

The method returns the following COM error codes. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
The clipboard contents or <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> can be pasted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The clipboard contents or <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> cannot be pasted.

</td>
</tr>
</table>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-copy">Copy</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>