---
UID: NF:tom.ITextRange.Copy
title: ITextRange::Copy (tom.h)
description: Copies the text to a data object.
helpviewer_keywords: ["Copy","Copy method [Windows Controls]","Copy method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","Copy method","ITextRange.Copy","ITextRange::Copy","_win32_ITextRange_Copy","_win32_ITextRange_Copy_cpp","controls.ITextRange_Copy","controls._win32_ITextRange_Copy","tom/ITextRange::Copy"]
old-location: controls\ITextRange_Copy.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\copy.htm
ms.date: 12/05/2018
ms.keywords: Copy, Copy method [Windows Controls], Copy method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],Copy method, ITextRange.Copy, ITextRange::Copy, _win32_ITextRange_Copy, _win32_ITextRange_Copy_cpp, controls.ITextRange_Copy, controls._win32_ITextRange_Copy, tom/ITextRange::Copy
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
 - ITextRange::Copy
 - tom/ITextRange::Copy
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
 - ITextRange.Copy
---

# ITextRange::Copy


## -description

Copies the text to a data object.

## -parameters

### -param pVar

Type: <b>VARIANT*</b>

The copied text. 
					<i>pVar</i>-&gt;ppunkVal is the out parameter for an 
					<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> provided that the following conditions exist: 
					

<ul>
<li>pVar-&gt;vt = (VT_UNKNOWN | VT_BYREF) </li>
<li>pVar is not null </li>
<li>pVar-&gt;ppunkVal is not null </li>
</ul>
Otherwise, the clipboard is used.

## -returns

Type: <b>HRESULT</b>

This method returns an 
						<b>HRESULT</b> value. If successful, it returns <b>S_OK</b>. Otherwise, it returns <b>E_OUTOFMEMORY</b>.

## -remarks

The <a href="/windows/desktop/api/tom/nf-tom-itextrange-cut">ITextRange::Cut</a>, 
				<b>ITextRange::Copy</b>, and <a href="/windows/desktop/api/tom/nf-tom-itextrange-paste">ITextRange::Paste</a> methods let you perform the usual 
				<b>Cut</b>, <b>Copy</b>, and 
				<b>Paste</b> operations on a range object using an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, thereby not changing the contents of the clipboard. Among clipboard formats typically supported are <b>CF_TEXT</b> and <b>CF_RTF</b>. In addition, private clipboard formats can be used to reference a text solution's own internal rich text formats.

To copy and replace plain text, you can use the <a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">ITextRange::GetText</a> 
				<b></b> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">ITextRange::SetText</a> 
				<b></b> methods. To copy formatted text from range r1 to range r2 without using the clipboard, you can use <b>Copy</b> and 
				<b>Paste</b> and also the <a href="/windows/desktop/api/tom/nf-tom-itextrange-getformattedtext">ITextRange::GetFormattedText</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-setformattedtext">ITextRange::SetFormattedText</a> methods, as shown in the following Microsoft Visual Basic example:

<code>r2.GetFormattedText = r1.GetFormattedText</code>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-cut">Cut</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getformattedtext">GetFormattedText</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-gettext">GetText</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-paste">Paste</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setformattedtext">SetFormattedText</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-settext">SetText</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>