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

# InvertRect function


## -description


The <b>InvertRect</b> function inverts a rectangle in a window by performing a logical NOT operation on the color values for each pixel in the rectangle's interior.


## -parameters




### -param hDC [in]

A handle to the device context.


### -param lprc [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the logical coordinates of the rectangle to be inverted.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



On monochrome screens, <b>InvertRect</b> makes white pixels black and black pixels white. On color screens, the inversion depends on how colors are generated for the screen. Calling <b>InvertRect</b> twice for the same rectangle restores the display to its previous colors.




## -see-also




<a href="https://msdn.microsoft.com/98ab34da-ea07-4446-a62e-509c849d95f9">
        FillRect
      </a>



<a href="https://msdn.microsoft.com/8909e85d-fa5b-4058-9e58-e027160ec381">Filled Shape Functions</a>



<a href="https://msdn.microsoft.com/78439288-a769-4aab-aee7-7a03396ccebc">Filled Shapes Overview</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">
        RECT
      </a>
 

 

