---
UID: NF:tom.ITextSelection.MoveDown
title: ITextSelection::MoveDown (tom.h)
description: Mimics the functionality of the Down Arrow and Page Down keys.
helpviewer_keywords: ["ITextSelection interface [Windows Controls]","MoveDown method","ITextSelection.MoveDown","ITextSelection::MoveDown","MoveDown","MoveDown method [Windows Controls]","MoveDown method [Windows Controls]","ITextSelection interface","_win32_ITextSelection_MoveDown","_win32_ITextSelection_MoveDown_cpp","controls.ITextSelection_MoveDown","controls._win32_ITextSelection_MoveDown","tom/ITextSelection::MoveDown"]
old-location: controls\ITextSelection_MoveDown.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\movedown.htm
ms.date: 12/05/2018
ms.keywords: ITextSelection interface [Windows Controls],MoveDown method, ITextSelection.MoveDown, ITextSelection::MoveDown, MoveDown, MoveDown method [Windows Controls], MoveDown method [Windows Controls],ITextSelection interface, _win32_ITextSelection_MoveDown, _win32_ITextSelection_MoveDown_cpp, controls.ITextSelection_MoveDown, controls._win32_ITextSelection_MoveDown, tom/ITextSelection::MoveDown
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
 - ITextSelection::MoveDown
 - tom/ITextSelection::MoveDown
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
 - ITextSelection.MoveDown
---

# ITextSelection::MoveDown


## -description

Mimics the functionality of the Down Arrow and Page Down keys.

## -parameters

### -param Unit

Type: <b>long</b>

Unit to use in the operation. It can be one of the following. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Corresponding key combination</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomLine</b></td>
<td>Down Arrow</td>
<td>Moves down one line. This is the default.</td>
</tr>
<tr>
<td><b>tomParagraph</b></td>
<td>Ctrl+Down Arrow</td>
<td>Moves down one paragraph.</td>
</tr>
<tr>
<td><b>tomScreen</b></td>
<td>Page Down</td>
<td>Moves down one screen.</td>
</tr>
<tr>
<td><b>tomWindow</b></td>
<td>Ctrl+Page Down</td>
<td>Moves to last character in window.</td>
</tr>
</table>

### -param Count

Type: <b>long</b>

Number of Units to move past. The default value is 1.

### -param Extend

Type: <b>long</b>

Flag that indicates how to change the selection. If 
					<i>Extend</i> is zero (or <b>tomMove</b>), the method collapses the selection to an insertion point and then moves. If 
					<i>Extend</i> is 1 (or <b>tomExtend</b>), the method moves the active end and leaves the other end alone. The default value is zero. A nonzero 
					<i>Extend</i> value corresponds to the Shift key being pressed in addition to the key combination described in 
					<i>Unit</i>.

### -param pDelta

Type: <b>long*</b>

Pointer to a variable that receives the actual count of units the insertion point or active end is moved down. Collapsing the selection counts as one unit. This parameter can be null.

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

The <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveup">ITextSelection::MoveUp</a> and <b>ITextSelection::MoveDown</b> methods are similar to the <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">ITextSelection::MoveLeft</a> and <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">ITextSelection::MoveRight</a> methods, except that they reflect the behavior of the Up Arrow, Down Arrow, Page Up, and Page Down keys on the cursor-keypad.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">MoveRight</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveup">MoveUp</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>