---
UID: NF:tom.ITextSelection.MoveRight
title: ITextSelection::MoveRight (tom.h)
description: Generalizes the functionality of the Right Arrow key.
helpviewer_keywords: ["ITextSelection interface [Windows Controls]","MoveRight method","ITextSelection.MoveRight","ITextSelection::MoveRight","MoveRight","MoveRight method [Windows Controls]","MoveRight method [Windows Controls]","ITextSelection interface","_win32_ITextSelection_MoveRight","_win32_ITextSelection_MoveRight_cpp","controls.ITextSelection_MoveRight","controls._win32_ITextSelection_MoveRight","tom/ITextSelection::MoveRight"]
old-location: controls\ITextSelection_MoveRight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\moveright.htm
ms.date: 12/05/2018
ms.keywords: ITextSelection interface [Windows Controls],MoveRight method, ITextSelection.MoveRight, ITextSelection::MoveRight, MoveRight, MoveRight method [Windows Controls], MoveRight method [Windows Controls],ITextSelection interface, _win32_ITextSelection_MoveRight, _win32_ITextSelection_MoveRight_cpp, controls.ITextSelection_MoveRight, controls._win32_ITextSelection_MoveRight, tom/ITextSelection::MoveRight
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
 - ITextSelection::MoveRight
 - tom/ITextSelection::MoveRight
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
 - ITextSelection.MoveRight
---

# ITextSelection::MoveRight


## -description

Generalizes the functionality of the Right Arrow key.

## -parameters

### -param Unit

Type: <b>long</b>

Unit to use. It can be one of the following. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Corresponding key combination</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomCharacter</b></td>
<td>Right Arrow</td>
<td>Move one character position to the right. This is the default.</td>
</tr>
<tr>
<td><b>tomWord</b></td>
<td>Ctrl+Right Arrow</td>
<td>Move one word to the right.</td>
</tr>
</table>
 

Note, if 
					<i>Count</i> is less than zero, movement is to the left.

### -param Count

Type: <b>long</b>

Number of Units to move past. The default value is 1. If <i>Count</i> is less than zero, movement is to the left.

### -param Extend

Type: <b>long</b>

Flag that indicates how to change the selection. If 
					<i>Extend</i> is zero (or <b>tomMove</b>), the method collapses the selection to an insertion point at the active end and then moves it. If <i>Extend</i> is 1 (or <b>tomExtend</b>), the method moves the active end and leaves the other end alone. The default value is zero. A nonzero <i>Extend</i> value corresponds to the Shift key being pressed in addition to the key combination described in <i>Unit</i>.

### -param pDelta

Type: <b>long*</b>

The actual count of units the insertion point or active end is moved left. This parameter can be null. Collapsing the selection, when <i>Extend</i> is 0, counts as one unit.

## -returns

Type: <b>HRESULT</b>

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Unit is not valid.

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

Microsoft WordBasic move methods like 
				<b>CharRight</b>, 
				<b>CharLeft</b>, 
				<b>WordRight</b>, and 
				<b>WordLeft</b> are hybrids that can do four things that are closely related to the standard arrow-key edit behavior: 

<ul>
<li>Move the current insertion point if there's no selection. </li>
<li>Move the active end of the selection if there is a selection. </li>
<li>Turn an insertion point into a selection and vice versa. </li>
<li>Return a Boolean stating if movement occurred. </li>
</ul>
The 
				<i>Extend</i> argument of <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a>  and <b>MoveRight</b> enables you to be consistent with the first three items above, and the 
				<i>pDelta</i> is a generalization of the fourth. For example, given a selection, s, consisting of a single range, you have the following correspondences (for left-to-right characters).

<table class="clsStd">
<tr>
<th>ITextSelection</th>
<th>WordBasic</th>
<th>Function</th>
</tr>
<tr>
<td>s.MoveRight tomWord, 1, 1</td>
<td>WordRight 1,1</td>
<td>Moves active end one word right.</td>
</tr>
<tr>
<td>s.MoveLeft tomCharacter, 1, 1</td>
<td>CharLeft 1,1</td>
<td>Moves active end one character left.</td>
</tr>
</table>
 

As in WordBasic, if 
				<i>Count</i> is less than zero, the meanings of left and right are interchanged, that is <code>MoveLeft (Unit, Count, Extend)</code> is equivalent to <code>MoveRight(Unit, -Count, Extend)</code>. 

Similar to WordBasic and the Right Arrow key UI behavior, calling <code>MoveRight(Unit, Count)</code> on a degenerate selection moves the insertion point the specified number of 
				units. On a degenerate range, calling <code>MoveRight(Unit, Count, 1)</code>  where <code>Count</code> is greater than zero causes the range to become nondegenerate with the right end being the active end.

When 
				<i>Extend</i> is <b>tomExtend</b> (or is nonzero), <b>MoveRight</b> moves only the active end of the selection, leaving the other end where it is. However, if 
				<i>Extend</i> equals zero and the selection starts as a nondegenerate range, <code>MoveRight(Unit, Count)</code> where <code>Count</code> is greater than zero moves the active end <code>Count</code> - 1 units right, and then moves the other end to the active end. In other words, it makes an insertion point at the active end. Collapsing the range counts as one 
				unit. Thus, <code>MoveRight(tomCharacter)</code> converts a nondegenerate selection into a degenerate one at the selection's right end. Here, <i>Count</i> has the default value of 1 and <i>Extend</i> has the default value of zero. This example corresponds to pressing the Right Arrow key. <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a> and <b>MoveRight</b> are related to the <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> move methods, but differ in that they explicitly use the active end (the end moved by pressing the Shift key).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>