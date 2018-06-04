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

# InvalidateRgn function


## -description


The <b>InvalidateRgn</b> function invalidates the client area within the specified region by adding it to the current update region of a window. The invalidated region, along with all other areas in the update region, is marked for painting when the next <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message occurs.


## -parameters




### -param hWnd [in]

A handle to the window with an update region that is to be modified.


### -param hRgn [in]

A handle to the region to be added to the update region. The region is assumed to have client coordinates. If this parameter is <b>NULL</b>, the entire client area is added to the update region.


### -param bErase [in]

Specifies whether the background within the update region should be erased when the update region is processed. If this parameter is <b>TRUE</b>, the background is erased when the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function is called. If the parameter is <b>FALSE</b>, the background remains unchanged.


## -returns



The return value is always nonzero.




## -remarks



Invalidated areas accumulate in the update region until the next <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message is processed or until the region is validated by using the <a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a> or <a href="https://msdn.microsoft.com/80fb1d4a-d9b1-4e67-b585-eee81893ed34">ValidateRgn</a> function.

The system sends a <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> message to a window whenever its update region is not empty and there are no other messages in the application queue for that window.

The specified region must have been created by using one of the region functions.

If the <i>bErase</i> parameter is <b>TRUE</b> for any part of the update region, the background in the entire region is erased, not just in the specified part.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/5a823d36-d08b-41c9-8857-540576f54b55">InvalidateRect</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/961dd768-1849-44df-bc7f-480881ed6477">ValidateRect</a>



<a href="https://msdn.microsoft.com/80fb1d4a-d9b1-4e67-b585-eee81893ed34">ValidateRgn</a>



<a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>
 

 

