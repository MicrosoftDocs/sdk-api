---
UID: NF:tom.ITextRange.MoveEnd
title: ITextRange::MoveEnd (tom.h)
description: Moves the end position of the range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","MoveEnd method","ITextRange.MoveEnd","ITextRange::MoveEnd","MoveEnd","MoveEnd method [Windows Controls]","MoveEnd method [Windows Controls]","ITextRange interface","_win32_ITextRange_MoveEnd","_win32_ITextRange_MoveEnd_cpp","controls.ITextRange_MoveEnd","controls._win32_ITextRange_MoveEnd","tom/ITextRange::MoveEnd"]
old-location: controls\ITextRange_MoveEnd.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\moveend.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],MoveEnd method, ITextRange.MoveEnd, ITextRange::MoveEnd, MoveEnd, MoveEnd method [Windows Controls], MoveEnd method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveEnd, _win32_ITextRange_MoveEnd_cpp, controls.ITextRange_MoveEnd, controls._win32_ITextRange_MoveEnd, tom/ITextRange::MoveEnd
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
 - ITextRange::MoveEnd
 - tom/ITextRange::MoveEnd
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
 - ITextRange.MoveEnd
---

# ITextRange::MoveEnd


## -description

Moves the end position of the range.

## -parameters

### -param Unit

Type: <b>long</b>

The units by which to move the end of the range. The default value is <b>tomCharacter</b>. For a list of the other unit values, see <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>.

### -param Count

Type: <b>long</b>

The number of units to move past. The default value is 1. If <i>Count</i> is greater than zero, motion is forward—toward the end of the story—and if <i>Count</i> is less than zero, motion is backward—toward the beginning. If  <i>Count</i> is zero, the end position is unchanged.

### -param pDelta

Type: <b>long*</b>

The actual number of units that the end position of the range is moved past. The value can be null.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Unit is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>

## -remarks

If the new end position precedes the old start position, the new start position is set equal to the new end position; that is, it becomes a degenerate range or an insertion point.

The motion described by <b>ITextRange::MoveEnd</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>