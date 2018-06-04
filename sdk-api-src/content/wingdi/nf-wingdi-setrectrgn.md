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

# SetRectRgn function


## -description


The <b>SetRectRgn</b> function converts a region into a rectangular region with the specified coordinates.


## -parameters




### -param hrgn [in]

Handle to the region.


### -param left

TBD


### -param top

TBD


### -param right

TBD


### -param bottom

TBD




#### - nBottomRect [in]

Specifies the y-coordinate of the lower-right corner of the rectangular region in logical units.


#### - nLeftRect [in]

Specifies the x-coordinate of the upper-left corner of the rectangular region in logical units.


#### - nRightRect [in]

Specifies the x-coordinate of the lower-right corner of the rectangular region in logical units.


#### - nTopRect [in]

Specifies the y-coordinate of the upper-left corner of the rectangular region in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The region does not include the lower and right boundaries of the rectangle.




## -see-also




<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

