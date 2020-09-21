---
UID: NF:tom.ITextFont.GetDuplicate
title: ITextFont::GetDuplicate (tom.h)
description: Gets a duplicate of this text font object.
helpviewer_keywords: ["GetDuplicate","GetDuplicate method [Windows Controls]","GetDuplicate method [Windows Controls]","ITextFont interface","ITextFont interface [Windows Controls]","GetDuplicate method","ITextFont.GetDuplicate","ITextFont::GetDuplicate","_win32_ITextFont_GetDuplicate","_win32_ITextFont_GetDuplicate_cpp","controls.ITextFont_GetDuplicate","controls._win32_ITextFont_GetDuplicate","tom/ITextFont::GetDuplicate"]
old-location: controls\ITextFont_GetDuplicate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont\itextfontgetduplicate.htm
ms.date: 12/05/2018
ms.keywords: GetDuplicate, GetDuplicate method [Windows Controls], GetDuplicate method [Windows Controls],ITextFont interface, ITextFont interface [Windows Controls],GetDuplicate method, ITextFont.GetDuplicate, ITextFont::GetDuplicate, _win32_ITextFont_GetDuplicate, _win32_ITextFont_GetDuplicate_cpp, controls.ITextFont_GetDuplicate, controls._win32_ITextFont_GetDuplicate, tom/ITextFont::GetDuplicate
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
 - ITextFont::GetDuplicate
 - tom/ITextFont::GetDuplicate
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
 - ITextFont.GetDuplicate
---

# ITextFont::GetDuplicate


## -description

Gets a duplicate of this text font object.

## -parameters

### -param ppFont

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>**</b>

The duplicate text font object.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the new object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The method includes an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The font object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -remarks

The duplicate property is the default property of an <a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> object.

For an example of how to use font duplicates, see <a href="/windows/desktop/api/tom/nf-tom-itextrange-setfont">SetFont</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextfont-setduplicate">SetDuplicate</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setfont">SetFont</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>