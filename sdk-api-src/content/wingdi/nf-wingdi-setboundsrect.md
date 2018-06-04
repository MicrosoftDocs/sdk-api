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

# SetBoundsRect function


## -description


The <b>SetBoundsRect</b> function controls the accumulation of bounding rectangle information for the specified device context. The system can maintain a bounding rectangle for all drawing operations. An application can examine and set this rectangle. The drawing boundaries are useful for invalidating bitmap caches.


## -parameters




### -param hdc [in]

A handle to the device context for which to accumulate bounding rectangles.


### -param lprect

TBD


### -param flags [in]

Specifies how the new rectangle will be combined with the accumulated rectangle. This parameter can be one of more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DCB_ACCUMULATE"></a><a id="dcb_accumulate"></a><dl>
<dt><b>DCB_ACCUMULATE</b></dt>
</dl>
</td>
<td width="60%">
Adds the rectangle specified by the <i>lprcBounds</i> parameter to the bounding rectangle (using a rectangle union operation). Using both DCB_RESET and DCB_ACCUMULATE sets the bounding rectangle to the rectangle specified by the <i>lprcBounds</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_DISABLE"></a><a id="dcb_disable"></a><dl>
<dt><b>DCB_DISABLE</b></dt>
</dl>
</td>
<td width="60%">
Turns off boundary accumulation.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_ENABLE"></a><a id="dcb_enable"></a><dl>
<dt><b>DCB_ENABLE</b></dt>
</dl>
</td>
<td width="60%">
Turns on boundary accumulation, which is disabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="DCB_RESET"></a><a id="dcb_reset"></a><dl>
<dt><b>DCB_RESET</b></dt>
</dl>
</td>
<td width="60%">
Clears the bounding rectangle.

</td>
</tr>
</table>
 


#### - lprcBounds [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure used to set the bounding rectangle. Rectangle dimensions are in logical coordinates. This parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value specifies the previous state of the bounding rectangle. This state can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DCB_DISABLE</td>
<td>Boundary accumulation is off.</td>
</tr>
<tr>
<td>DCB_ENABLE</td>
<td>Boundary accumulation is on. DCB_ENABLE and DCB_DISABLE are mutually exclusive.</td>
</tr>
<tr>
<td>DCB_RESET</td>
<td>Bounding rectangle is empty.</td>
</tr>
<tr>
<td>DCB_SET</td>
<td>Bounding rectangle is not empty. DCB_SET and DCB_RESET are mutually exclusive.</td>
</tr>
</table>
 

If the function fails, the return value is zero.




## -remarks



The DCB_SET value is a combination of the bit values DCB_ACCUMULATE and DCB_RESET. Applications that check the DCB_RESET bit to determine whether the bounding rectangle is empty must also check the DCB_ACCUMULATE bit. The bounding rectangle is empty only if the DCB_RESET bit is 1 and the DCB_ACCUMULATE bit is 0.




## -see-also




<a href="https://msdn.microsoft.com/139d4550-9adc-48b3-a15c-03ae1f1ef1ab">GetBoundsRect</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>
 

 

