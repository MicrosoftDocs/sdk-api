---
UID: NF:msinkaut.IInkPicture.SetGestureStatus
title: IInkPicture::SetGestureStatus
author: windows-sdk-content
description: Modifies the interest of the object or control in a known gesture.
old-location: tablet\inkpicture_setgesturestatus.htm
tech.root: tablet
ms.assetid: 36f3611a-c7d9-49a2-9ead-db98647f6da7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 7bab227f-d095-48e8-856f-6446e62826dd, IInkPicture, IInkPicture interface [Tablet PC],SetGestureStatus method, IInkPicture.SetGestureStatus, IInkPicture::SetGestureStatus, SetGestureStatus, SetGestureStatus method [Tablet PC], SetGestureStatus method [Tablet PC],IInkPicture interface, msinkaut/IInkPicture::SetGestureStatus, tablet.inkpicture_setgesturestatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkPicture.SetGestureStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkPicture::SetGestureStatus


## -description



Modifies the interest of the object or control in a known gesture.




## -parameters




### -param Gesture [in]

The gesture that you want to set the status of.


### -param Listen [in]

VARIANT_TRUE to indicate that the gesture is being used; VARIANT_FALSE to indicate the gesture is being ignored.


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
InkCollector collection mode must be in gesture mode.

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



To get the interest of the object or control in a known gesture, call the <a href="https://msdn.microsoft.com/b4ccc35d-35b5-4633-acc9-efd4c7eb05e3">GetGestureStatus</a> method.

The <a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">IAG_AllGestures</a> gesture ID is not supported by the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control and returns an error. Passing invalid Gesture IDs does not return an error for InkEdit, but fails for <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, and <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>.

For the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, this method should only be called if the <a href="https://msdn.microsoft.com/47a41d5c-2598-4dfc-a5b5-af4df7fdaa6d">Status</a> property returns <a href="https://msdn.microsoft.com/94c3a863-4c8a-4471-be1b-b4d5f8ded374">IES_Idle</a>.




## -see-also




<a href="https://msdn.microsoft.com/a20f2d78-6cfe-4755-968e-91369021db1b">Gesture Event</a>



<a href="https://msdn.microsoft.com/b4ccc35d-35b5-4633-acc9-efd4c7eb05e3">GetGestureStatus Method</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">InkApplicationGesture Enumeration</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>
 

 

