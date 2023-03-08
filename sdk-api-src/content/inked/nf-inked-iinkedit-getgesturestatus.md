---
UID: NF:inked.IInkEdit.GetGestureStatus
title: IInkEdit::GetGestureStatus (inked.h)
description: Indicates whether the InkEdit control is interested in a particular application gesture.
helpviewer_keywords: ["0992dbd2-bd32-4af6-abd1-66027dd2b30f","GetGestureStatus","GetGestureStatus method [Tablet PC]","GetGestureStatus method [Tablet PC]","IInkEdit interface","IInkEdit interface [Tablet PC]","GetGestureStatus method","IInkEdit.GetGestureStatus","IInkEdit::GetGestureStatus","inked/IInkEdit::GetGestureStatus","tablet.inkedit_getgesturestatus"]
old-location: tablet\inkedit_getgesturestatus.htm
tech.root: tablet
ms.assetid: 0992dbd2-bd32-4af6-abd1-66027dd2b30f
ms.date: 12/05/2018
ms.keywords: 0992dbd2-bd32-4af6-abd1-66027dd2b30f, GetGestureStatus, GetGestureStatus method [Tablet PC], GetGestureStatus method [Tablet PC],IInkEdit interface, IInkEdit interface [Tablet PC],GetGestureStatus method, IInkEdit.GetGestureStatus, IInkEdit::GetGestureStatus, inked/IInkEdit::GetGestureStatus, tablet.inkedit_getgesturestatus
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkEd.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkEdit::GetGestureStatus
 - inked/IInkEdit::GetGestureStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkEd.dll
 - InkEd.dll.dll
api_name:
 - IInkEdit.GetGestureStatus
---

# IInkEdit::GetGestureStatus


## -description

Indicates whether the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is interested in a particular application gesture.

## -parameters

### -param Gesture [in]

The gesture that you want the status of.

### -param pListen [out, retval]

<b>VARIANT_TRUE</b> if the <a href="/windows/desktop/tablet/inkedit-control">InkEdit</a> control has interest in the gesture and the <a href="/windows/desktop/tablet/inkedit-gesture">Gesture</a> event of the InkEdit control fires when the gesture is recognized. <b>VARIANT_FALSE</b> if the InkEdit control has no interest in the gesture.

## -returns

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Input parameter was incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INVALID_MODE</b></dt>
</dl>
</td>
<td width="60%">
Collection mode must be in gesture-mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to perform action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The flag is invalid.

</td>
</tr>
</table>

## -remarks

This method throws an exception if the <i>gesture</i> parameter is set to the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_AllGestures</a> gesture.

To set the interest of the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control in a particular gesture, call the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus">SetGestureStatus</a> method.

<div class="alert"><b>Note</b>  By default, the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control has interest in the following gestures:</div>
<div> </div>
<ul>
<li>
<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_Left</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_Right</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_UpRightLong</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_DownLeftLong</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_UpRight</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_DownLeft</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/tablet/inkedit-gesture">Gesture Event [InkEdit Control]</a>



<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>



<a href="/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus">SetGestureStatus Method [InkEdit Control]</a>
