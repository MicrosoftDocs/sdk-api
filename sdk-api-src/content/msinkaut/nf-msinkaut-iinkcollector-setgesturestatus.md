---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



To get the interest of the object or control in a known gesture, call the <a href="https://msdn.microsoft.com/31973709-1702-4ec1-8228-b0d1bdb64bc8">GetGestureStatus</a> method.

The <a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">IAG_AllGestures</a> gesture ID is not supported by the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control and returns an error. Passing invalid Gesture IDs does not return an error for InkEdit, but fails for <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>, <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a>, and <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a>.

For the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, this method should only be called if the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> property returns <a href="https://msdn.microsoft.com/94c3a863-4c8a-4471-be1b-b4d5f8ded374">IES_Idle</a>.




## -see-also




<a href="https://msdn.microsoft.com/5830f7f8-2870-4194-ab3e-b63b71e97063">Gesture Event</a>



<a href="https://msdn.microsoft.com/31973709-1702-4ec1-8228-b0d1bdb64bc8">GetGestureStatus Method</a>



<a href="tablet.iinkcollector">IInkCollector</a>



<a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">InkApplicationGesture Enumeration</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>
 

 

