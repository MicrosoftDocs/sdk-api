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

# Pie function


## -description


The <b>Pie</b> function draws a pie-shaped wedge bounded by the intersection of an ellipse and two radials. The pie is outlined by using the current pen and filled by using the current brush.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param left

TBD


### -param top

TBD


### -param right

TBD


### -param bottom

TBD


### -param xr1

TBD


### -param yr1

TBD


### -param xr2

TBD


### -param yr2

TBD




#### - nBottomRect [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


#### - nLeftRect [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


#### - nRightRect [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


#### - nTopRect [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


#### - nXRadial1 [in]

The x-coordinate, in logical coordinates, of the endpoint of the first radial.


#### - nXRadial2 [in]

The x-coordinate, in logical coordinates, of the endpoint of the second radial.


#### - nYRadial1 [in]

The y-coordinate, in logical coordinates, of the endpoint of the first radial.


#### - nYRadial2 [in]

The y-coordinate, in logical coordinates, of the endpoint of the second radial.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The curve of the pie is defined by an ellipse that fits the specified bounding rectangle. The curve begins at the point where the ellipse intersects the first radial and extends counterclockwise to the point where the ellipse intersects the second radial.

The current position is neither used nor updated by the <b>Pie</b> function.




## -see-also




<a href="https://msdn.microsoft.com/65c38da1-ab7d-4e80-83e3-ba1db66f8fd9">
        AngleArc
      </a>



<a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">
        Arc
      </a>



<a href="https://msdn.microsoft.com/5e358a14-9f39-4267-9a44-c8bf05b5dfbb">
        ArcTo
      </a>



<a href="https://msdn.microsoft.com/d6752c47-96a5-4fac-a1bb-0611a91f03f9">
        Chord
      </a>



<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>
 

 

