---
UID: NF:msinkaut.IInkOverlay.GetGestureStatus
title: IInkOverlay::GetGestureStatus (msinkaut.h)
description: Retrieves a value that determines whether the InkCollector or InkOverlay object is interested in a particular application gesture.
helpviewer_keywords: ["31973709-1702-4ec1-8228-b0d1bdb64bc8","GetGestureStatus","GetGestureStatus method [Tablet PC]","GetGestureStatus method [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","GetGestureStatus method","IInkOverlay.GetGestureStatus","IInkOverlay::GetGestureStatus","msinkaut/IInkOverlay::GetGestureStatus","tablet.inkoverlay_getgesturestatus"]
old-location: tablet\inkoverlay_getgesturestatus.htm
tech.root: tablet
ms.assetid: fdf4ce5b-0a3f-441b-bead-6297ea6c8f5e
ms.date: 12/05/2018
ms.keywords: 31973709-1702-4ec1-8228-b0d1bdb64bc8, GetGestureStatus, GetGestureStatus method [Tablet PC], GetGestureStatus method [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],GetGestureStatus method, IInkOverlay.GetGestureStatus, IInkOverlay::GetGestureStatus, msinkaut/IInkOverlay::GetGestureStatus, tablet.inkoverlay_getgesturestatus
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
 - IInkOverlay::GetGestureStatus
 - msinkaut/IInkOverlay::GetGestureStatus
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
 - IInkOverlay.GetGestureStatus
---

# IInkOverlay::GetGestureStatus


## -description

Retrieves a value that determines whether the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object is interested in a particular application gesture.

## -parameters

### -param Gesture [in]

The gesture that you want the status of.

### -param Listening [out, retval]

<b>VARIANT_TRUE</b> if the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> control has interest in a particular application gesture; otherwise, <b>VARIANT_FALSE</b>.

This method returns a value that indicates the interest of the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object in a known application gesture. If <b>VARIANT_TRUE</b>, the <b>InkCollector</b> or <b>InkOverlay</b> object is interested in the gesture and the <a href="/windows/desktop/tablet/inkcollector-gesture">Gesture</a> event of the <b>InkCollector</b> or <b>InkOverlay</b> object fires when the gesture is recognized.

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

This method throws an exception if the <i>gesture</i> parameter is set to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">IAG_AllGestures</a>.

To set the interest of the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> or <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object in a particular gesture, call the <b>InkCollector</b> or <b>InkOverlay</b> object's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus">SetGestureStatus</a> method.

<div class="alert"><b>Note</b>  By default, the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> and <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> objects do not have interest in any of the application gestures.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/tablet/inkcollector-gesture">Gesture Event</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus">SetGestureStatus Method</a>
