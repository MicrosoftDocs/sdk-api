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

# Rectangle function


## -description


The <b>Rectangle</b> function draws a rectangle. The rectangle is outlined by using the current pen and filled by using the current brush.


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

The y-coordinate, in logical coordinates, of the lower-right corner of the rectangle.


#### - nLeftRect [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the rectangle.


#### - nRightRect [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the rectangle.


#### - nTopRect [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the rectangle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The current position is neither used nor updated by <b>Rectangle</b>.

The rectangle that is drawn excludes the bottom and right edges.

If a PS_NULL pen is used, the dimensions of the rectangle are 1 pixel less in height and 1 pixel less in width.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/c5fc3346-e5d7-49c0-979b-10d91ab965c5">Using Filled Shapes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>



<a href="https://msdn.microsoft.com/17808a6a-7bd0-4fd6-81ab-00d5db764b93">
        RoundRect
      </a>
 

 

