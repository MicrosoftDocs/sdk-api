---
UID: NF:msinkaut.IInkOverlay.GetGestureStatus
title: IInkOverlay::GetGestureStatus
author: windows-sdk-content
description: Retrieves a value that determines whether the InkCollector or InkOverlay object is interested in a particular application gesture.
old-location: tablet\inkoverlay_getgesturestatus.htm
old-project: tablet
ms.assetid: fdf4ce5b-0a3f-441b-bead-6297ea6c8f5e
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 31973709-1702-4ec1-8228-b0d1bdb64bc8, GetGestureStatus, GetGestureStatus method [Tablet PC], GetGestureStatus method [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],GetGestureStatus method, IInkOverlay.GetGestureStatus, IInkOverlay::GetGestureStatus, msinkaut/IInkOverlay::GetGestureStatus, tablet.inkoverlay_getgesturestatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkOverlay::GetGestureStatus


## -description



Retrieves a value that determines whether the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object is interested in a particular application gesture.




## -parameters




### -param Gesture [in]

The gesture that you want the status of.


### -param Listening [out, retval]

<b>VARIANT_TRUE</b> if the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> control has interest in a particular application gesture; otherwise, <b>VARIANT_FALSE</b>.

This method returns a value that indicates the interest of the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object in a known application gesture. If <b>VARIANT_TRUE</b>, the <b>InkCollector</b> or <b>InkOverlay</b> object is interested in the gesture and the <a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture</a> event of the <b>InkCollector</b> or <b>InkOverlay</b> object fires when the gesture is recognized.


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



This method throws an exception if the <i>gesture</i> parameter is set to <a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">IAG_AllGestures</a>.

To set the interest of the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> or <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object in a particular gesture, call the <b>InkCollector</b> or <b>InkOverlay</b> object's <a href="https://msdn.microsoft.com/7bab227f-d095-48e8-856f-6446e62826dd">SetGestureStatus</a> method.

<div class="alert"><b>Note</b>  By default, the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> and <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> objects do not have interest in any of the application gestures.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture Event</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846799(v=VS.85).aspx">IInkOverlay</a>



<a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">InkApplicationGesture Enumeration</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/7bab227f-d095-48e8-856f-6446e62826dd">SetGestureStatus Method</a>
 

 

