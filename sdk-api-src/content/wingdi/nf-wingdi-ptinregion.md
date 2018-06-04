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

# PtInRegion function


## -description


The <b>PtInRegion</b> function determines whether the specified point is inside the specified region.


## -parameters




### -param hrgn [in]

Handle to the region to be examined.


### -param x

TBD


### -param y

TBD




#### - X [in]

Specifies the x-coordinate of the point in logical units.


#### - Y [in]

Specifies the y-coordinate of the point in logical units.


## -returns



If the specified point is in the region, the return value is nonzero.

If the specified point is not in the region, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/198a02f1-120c-4f65-aa7c-a41f2e5e81a9">RectInRegion</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

