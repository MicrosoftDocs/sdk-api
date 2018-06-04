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

# InvertRgn function


## -description


The <b>InvertRgn</b> function inverts the colors in the specified region.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param hrgn [in]

Handle to the region for which colors are inverted. The region's coordinates are presumed to be logical coordinates.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



On monochrome screens, the <b>InvertRgn</b> function makes white pixels black and black pixels white. On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/64cd6e82-7a0d-4b5e-b491-450f37eea43a">Using Brushes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c4e0eca5-442b-462b-a4f2-0c628b6d3d38">FillRgn</a>



<a href="https://msdn.microsoft.com/7656fb67-d865-459e-b379-4f2e44c76fd0">PaintRgn</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

