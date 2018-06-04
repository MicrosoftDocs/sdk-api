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

# WNDOBJ_cEnumStart function


## -description


The <b>WNDOBJ_cEnumStart</b> function is a callback function that sets parameters for enumeration of rectangles in the visible region of a window.


## -parameters




### -param pwo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a> structure created by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>.


### -param iType

Specifies the type of structures to be returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff570602">WNDOBJ_bEnum</a>. This parameter can be CT_RECTANGLES, meaning that the region is to be enumerated as a list of rectangles.


### -param iDirection

Determines the order in which the rectangles are returned. This order can be essential when an overlapping <a href="https://msdn.microsoft.com/library/windows/hardware/ff556180">DrvBitBlt</a> is being performed on the same surface. If the order is not relevant to the device driver, then CD_ANY should be specified. This allows GDI to optimize its enumeration for complex regions. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
CD_ANY

</td>
<td>
Any order convenient for GDI.

</td>
</tr>
<tr>
<td>
CD_LEFTDOWN

</td>
<td>
Right to left, top to bottom.

</td>
</tr>
<tr>
<td>
CD_LEFTUP

</td>
<td>
Right to left, bottom to top.

</td>
</tr>
<tr>
<td>
CD_LEFTWARDS

</td>
<td>
Left to right, vertical direction is not defined.

</td>
</tr>
<tr>
<td>
CD_RIGHTDOWN

</td>
<td>
Left to right, top to bottom.

</td>
</tr>
<tr>
<td>
CD_RIGHTUP

</td>
<td>
Left to right, bottom to top.

</td>
</tr>
<tr>
<td>
CD_UPWARDS

</td>
<td>
Bottom to top, horizontal direction is not defined.

</td>
</tr>
</table>
 


### -param cLimit

Is an indication of how many objects the driver is interested in caching. This is only used to decide when to stop counting rectangles while GDI is calculating the return value for this function. If <i>cLimit</i> is zero, counting is not done.


## -returns



The return value is a count of the number of objects that would be enumerated, provided this value is less than or equal to <i>cLimit</i>. If the count is greater than <i>cLimit</i>, the return value is 0xFFFFFFFF.




## -remarks



Enumeration can be restarted by calling this function again.

<b>WNDOBJ_cEnumStart</b> should be called only:

<ul>
<li>
In the context of the driver callback function supplied to GDI in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a> function, or the graphics DDI functions where a WNDOBJ is given. 

</li>
<li>
When the calling thread has the device lock to ensure that no client region changes occur.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556180">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564769">EngCreateWnd</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564967">EngLockDriverObj</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570599">WNDOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570602">WNDOBJ_bEnum</a>
 

 

