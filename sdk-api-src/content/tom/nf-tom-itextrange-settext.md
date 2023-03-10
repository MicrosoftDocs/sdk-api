---
UID: NF:tom.ITextRange.SetText
title: ITextRange::SetText (tom.h)
description: Sets the text in this range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","SetText method","ITextRange.SetText","ITextRange::SetText","SetText","SetText method [Windows Controls]","SetText method [Windows Controls]","ITextRange interface","_win32_ITextRange_SetText","_win32_ITextRange_SetText_cpp","controls.ITextRange_SetText","controls._win32_ITextRange_SetText","tom/ITextRange::SetText"]
old-location: controls\ITextRange_SetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\settext.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],SetText method, ITextRange.SetText, ITextRange::SetText, SetText, SetText method [Windows Controls], SetText method [Windows Controls],ITextRange interface, _win32_ITextRange_SetText, _win32_ITextRange_SetText_cpp, controls.ITextRange_SetText, controls._win32_ITextRange_SetText, tom/ITextRange::SetText
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
 - ITextRange::SetText
 - tom/ITextRange::SetText
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
 - ITextRange.SetText
---

# ITextRange::SetText


## -description

Sets the text in this range.

## -parameters

### -param bstr [in]

Type: <b>BSTR</b>

Text that replaces the current text in this range. If null, the current text is deleted.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
Text is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
bstr is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

<b>ITextRange::SetText</b> replaces the text in the range with the new text. In contrast, <a href="/windows/desktop/api/tom/nf-tom-itextselection-typetext">TypeText</a> replaces the selection with the text <i>bstr</i> and leaves the selection as an insertion point just following the inserted text, just as if you had typed the text in. For UI selection behavior, see <b>TypeText</b>.

If, after you call <b>ITextRange::SetText</b>, you call <a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">ITextRange::GetText</a>, you get back the same text that you set with the <b>ITextRange::SetText</b> method (unless some other range has changed that text in between the calls).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">GetText</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-typetext">TypeText</a>