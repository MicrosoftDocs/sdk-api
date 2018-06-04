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

# IInkGesture::GetHotPoint


## -description



Gets the hot point of the gesture, in ink space coordinates.




## -parameters




### -param X [in, out]

The X-value of the hot point, in ink space coordinates.


### -param Y [in, out]

The Y-value of the hot point, in ink space coordinates.


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
Error information is provided.

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
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
</table>
 




## -remarks



The hot point is the one distinguishing point of a gesture. It is usually the point of the angle in a gesture or the point at which the gesture is intended to occur in relation to the content around it. If there is no discernable hot point for a known gesture, the starting point of the gesture is the hot point.

For example, the hot point of the <a href="https://msdn.microsoft.com/b429ec96-691f-4761-92bf-ef500cf0e1be">Check</a> gesture is the point of the angle, and the hot point of the <b>Curlicue</b> gesture is the start of the stroke that is the gesture.

For more information about how a hot point is used, see <a href="https://msdn.microsoft.com/5bc80086-7acf-4f86-a9fb-a663de489f8b">Using Gestures</a>.




## -see-also




<a href="https://msdn.microsoft.com/87a1db34-371e-4c02-a470-55f35dfbf4ab">IInkGesture Interface</a>



<a href="https://msdn.microsoft.com/5bc80086-7acf-4f86-a9fb-a663de489f8b">Using Gestures</a>
 

 

