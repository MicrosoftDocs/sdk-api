---
UID: NF:inked.IInkEdit.SetGestureStatus
title: IInkEdit::SetGestureStatus (inked.h)
description: Modifies the interest of the InkEdit control in a known application gesture.
helpviewer_keywords: ["1fc9daa5-ee34-409b-b977-0d39b23d422e","IInkEdit interface [Tablet PC]","SetGestureStatus method","IInkEdit.SetGestureStatus","IInkEdit::SetGestureStatus","SetGestureStatus","SetGestureStatus method [Tablet PC]","SetGestureStatus method [Tablet PC]","IInkEdit interface","inked/IInkEdit::SetGestureStatus","tablet.inkedit_setgesturestatus"]
old-location: tablet\inkedit_setgesturestatus.htm
tech.root: tablet
ms.assetid: 1fc9daa5-ee34-409b-b977-0d39b23d422e
ms.date: 12/05/2018
ms.keywords: 1fc9daa5-ee34-409b-b977-0d39b23d422e, IInkEdit interface [Tablet PC],SetGestureStatus method, IInkEdit.SetGestureStatus, IInkEdit::SetGestureStatus, SetGestureStatus, SetGestureStatus method [Tablet PC], SetGestureStatus method [Tablet PC],IInkEdit interface, inked/IInkEdit::SetGestureStatus, tablet.inkedit_setgesturestatus
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
 - IInkEdit::SetGestureStatus
 - inked/IInkEdit::SetGestureStatus
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
 - IInkEdit.SetGestureStatus
---

# IInkEdit::SetGestureStatus


## -description

Modifies the interest of the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control in a known application gesture.

## -parameters

### -param Gesture [in]

The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture">IInkGesture</a> object that you want the status of.

### -param Listen [in]

<b>VARIANT_TRUE</b> to indicate that the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control uses the application gesture; otherwise, <b>VARIANT_FALSE</b>.

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
The input parameter was incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INVALID_MODE</b></dt>
</dl>
</td>
<td width="60%">
InkEdit status must be IES_Idle.

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
<dt><b>TPC_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
Unsupported gesture.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_AllGestures</a> gesture is not supported by the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control and returns an error. Passing invalid gesture identifiers does not return an error.

This method should only be called if the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a> property returns IES_Idle.

To get the interest of the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control in a known gesture, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus">GetGestureStatus</a> method.

## -see-also

<a href="/windows/desktop/tablet/inkedit-gesture">Gesture Event</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus">GetGestureStatus Method [InkEdit Control]</a>



<a href="../inked/nn-inked-iinkedit.md">IInkEdit</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a>



<a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
