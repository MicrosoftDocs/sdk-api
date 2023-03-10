---
UID: NF:tom.ITextRange.MoveStart
title: ITextRange::MoveStart (tom.h)
description: Moves the start position of the range the specified number of units in the specified direction.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","MoveStart method","ITextRange.MoveStart","ITextRange::MoveStart","MoveStart","MoveStart method [Windows Controls]","MoveStart method [Windows Controls]","ITextRange interface","_win32_ITextRange_MoveStart","_win32_ITextRange_MoveStart_cpp","controls.ITextRange_MoveStart","controls._win32_ITextRange_MoveStart","tom/ITextRange::MoveStart"]
old-location: controls\ITextRange_MoveStart.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\movestart.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],MoveStart method, ITextRange.MoveStart, ITextRange::MoveStart, MoveStart, MoveStart method [Windows Controls], MoveStart method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveStart, _win32_ITextRange_MoveStart_cpp, controls.ITextRange_MoveStart, controls._win32_ITextRange_MoveStart, tom/ITextRange::MoveStart
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
 - ITextRange::MoveStart
 - tom/ITextRange::MoveStart
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
 - ITextRange.MoveStart
---

# ITextRange::MoveStart


## -description

Moves the start position of the range the specified number of units in the specified direction.

## -parameters

### -param Unit

Type: <b>long</b>

Unit used in the move. The default value is <b>tomCharacter</b>. For a list of the other <i>Unit</i> values, see the discussion under <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>.

### -param Count

Type: <b>long</b>

Number of units to move. The default value is 1. If <i>Count</i> is greater than zero, motion is forward—toward the end of the story—and if <i>Count</i> is less than zero, motion is backward—toward the beginning. If  <i>Count</i> is zero, the start position is unchanged.

### -param pDelta

Type: <b>long*</b>

The actual number of units that the end is moved. The value can be null.

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

If the new start follows the old end, the new end is set equal to the new start.

The motion described by <b>ITextRange::MoveStart</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-moveend">MoveEnd</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>