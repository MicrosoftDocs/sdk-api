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

# FloodFill function


## -description


The <b>FloodFill</b> function fills an area of the display surface with the current brush. The area is assumed to be bounded as specified by the <i>crFill</i> parameter.
<div class="alert"><b>Note</b>  The <b>FloodFill</b> function is included only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/b996d47d-5aaf-4b13-8643-209744e5a04b">ExtFloodFill</a> function with FLOODFILLBORDER specified.</div><div> </div>

## -parameters




### -param hdc [in]

A handle to a device context.


### -param x

TBD


### -param y

TBD


### -param color

TBD




#### - crFill [in]

The color of the boundary or the area to be filled. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


#### - nXStart [in]

The x-coordinate, in logical units, of the point where filling is to start.


#### - nYStart [in]

The y-coordinate, in logical units, of the point where filling is to start.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The following are reasons this function might fail:

<ul>
<li>The fill could not be completed.</li>
<li>The given point has the boundary color specified by the <i>crFill</i> parameter.</li>
<li>The given point lies outside the current clipping regionthat is, it is not visible on the device.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ef3abc8a-5d95-41d0-8eb6-47719d472414">Bitmap Functions</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">
        COLORREF
      </a>



<a href="https://msdn.microsoft.com/b996d47d-5aaf-4b13-8643-209744e5a04b">
        ExtFloodFill
      </a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">
        RGB
      </a>
 

 

