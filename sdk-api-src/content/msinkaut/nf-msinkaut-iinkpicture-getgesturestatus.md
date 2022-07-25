---
UID: NF:msinkaut.IInkPicture.GetGestureStatus
title: IInkPicture::GetGestureStatus (msinkaut.h)
description: Retrieves a value that indicates whether the InkPicture control has interest in a particular application gesture.
helpviewer_keywords: ["GetGestureStatus","GetGestureStatus method [Tablet PC]","GetGestureStatus method [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","GetGestureStatus method","IInkPicture.GetGestureStatus","IInkPicture::GetGestureStatus","b4ccc35d-35b5-4633-acc9-efd4c7eb05e3","msinkaut/IInkPicture::GetGestureStatus","tablet.inkpicture_getgesturestatus"]
old-location: tablet\inkpicture_getgesturestatus.htm
tech.root: tablet
ms.assetid: b4ccc35d-35b5-4633-acc9-efd4c7eb05e3
ms.date: 12/05/2018
ms.keywords: GetGestureStatus, GetGestureStatus method [Tablet PC], GetGestureStatus method [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],GetGestureStatus method, IInkPicture.GetGestureStatus, IInkPicture::GetGestureStatus, b4ccc35d-35b5-4633-acc9-efd4c7eb05e3, msinkaut/IInkPicture::GetGestureStatus, tablet.inkpicture_getgesturestatus
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
 - IInkPicture::GetGestureStatus
 - msinkaut/IInkPicture::GetGestureStatus
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
 - IInkPicture.GetGestureStatus
---

# IInkPicture::GetGestureStatus


## -description

Retrieves a value that indicates whether the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has interest in a particular application gesture.

## -parameters

### -param Gesture [in]

The gesture that you want the status of.

### -param Listening [out, retval]

<b>VARIANT_TRUE</b> if the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control has interest in the gesture and the <a href="/windows/desktop/tablet/inkpicture-gesture">Gesture Event</a> fires when the gesture is recognized. <b>VARIANT_FALSE</b> if the InkPicture control has no interest in the gesture, and the strokes that were recognized as a gesture remain as <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> objects.

## -returns

This method can return one of these values.

<table>
<tr>
<th>HRESULT value</th>
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

To set the interest of the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control in a particular gesture, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus">SetGestureStatus Method</a>.

<div class="alert"><b>Note</b>  By default, the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control does not have interest in any application gesture.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/tablet/inkpicture-gesture">Gesture Event</a>



<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture">InkApplicationGesture Enumeration</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus">SetGestureStatus Method</a>
