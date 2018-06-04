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

# Ellipse function


## -description


The <b>Ellipse</b> function draws an ellipse. The center of the ellipse is the center of the specified bounding rectangle. The ellipse is outlined by using the current pen and is filled by using the current brush.


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




#### - nBottomRect [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


#### - nLeftRect [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


#### - nRightRect [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.


#### - nTopRect [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The current position is neither used nor updated by <b>Ellipse</b>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c5fc3346-e5d7-49c0-979b-10d91ab965c5">Using Filled Shapes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac">
        Arc
      </a>



<a href="https://msdn.microsoft.com/5e358a14-9f39-4267-9a44-c8bf05b5dfbb">
        ArcTo
      </a>



<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>
 

 

