---
UID: NF:msinkaut.IInkCollector.SetGestureStatus
title: IInkCollector::SetGestureStatus (msinkaut.h)
description: Modifies the interest of the object or control in a known gesture. (IInkCollector.SetGestureStatus)
helpviewer_keywords: ["7bab227f-d095-48e8-856f-6446e62826dd","IInkCollector interface [Tablet PC]","SetGestureStatus method","IInkCollector.SetGestureStatus","IInkCollector::SetGestureStatus","SetGestureStatus","SetGestureStatus method [Tablet PC]","SetGestureStatus method [Tablet PC]","IInkCollector interface","msinkaut/IInkCollector::SetGestureStatus","tablet.inkcollector_setgesturestatus"]
old-location: tablet\inkcollector_setgesturestatus.htm
tech.root: tablet
ms.assetid: 7bab227f-d095-48e8-856f-6446e62826dd
ms.date: 12/05/2018
ms.keywords: 7bab227f-d095-48e8-856f-6446e62826dd, IInkCollector interface [Tablet PC],SetGestureStatus method, IInkCollector.SetGestureStatus, IInkCollector::SetGestureStatus, SetGestureStatus, SetGestureStatus method [Tablet PC], SetGestureStatus method [Tablet PC],IInkCollector interface, msinkaut/IInkCollector::SetGestureStatus, tablet.inkcollector_setgesturestatus
req.header: msinkaut.h
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkCollector::SetGestureStatus
 - msinkaut/IInkCollector::SetGestureStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkCollector.SetGestureStatus
---

# IInkCollector::SetGestureStatus


## -description

Modifies the interest of the object or control in a known gesture.

## -parameters

### -param Gesture [in]

The gesture that you want to set the status of.

### -param Listen [in]

<b>VARIANT_TRUE</b> to indicate that the gesture is being used or <b>VARIANT_FALSE</b> if it is being ignored.

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
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INVALID_MODE</b></dt>
</dl>
</td>
<td width="60%">
The InkCollector collection mode must be in gesture mode.

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

To get the interest of the object or control in a known gesture, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus">GetGestureStatus</a> method.

The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_AllGestures</a> gesture ID is not supported by the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control and returns an error. Passing invalid Gesture IDs does not return an error for InkEdit, but fails for <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, and <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>.

For the <a href="/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, this method should only be called if the <a href="/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a> property returns <a href="/windows/desktop/api/inked/ne-inked-inkeditstatus">IES_Idle</a>.

## -see-also

<a href="/windows/desktop/tablet/inkcollector-gesture">Gesture Event</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-getgesturestatus">GetGestureStatus Method</a>



<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>
