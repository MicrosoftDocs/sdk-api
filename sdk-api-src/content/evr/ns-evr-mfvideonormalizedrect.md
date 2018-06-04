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

# MFVideoNormalizedRect structure


## -description



Defines a normalized rectangle, which is used to specify sub-rectangles in a video rectangle. When a rectangle N is <i>normalized</i> relative to some other rectangle R, it means the following:

<ul>
<li>
The coordinate (0.0, 0.0) on N is mapped to the upper-left corner of R.

</li>
<li>
The coordinate (1.0, 1.0) on N is mapped to the lower-right corner of R.

</li>
</ul>
Any coordinates of N that fall outside the range [0...1] are mapped to positions outside the rectangle R. A normalized rectangle can be used to specify a region within a video rectangle without knowing the resolution or even the aspect ratio of the video. For example, the upper-left quadrant is defined as {0.0, 0.0, 0.5, 0.5}.




## -struct-fields




### -field left

X-coordinate of the upper-left corner of the rectangle.


### -field top

Y-coordinate of the upper-left corner of the rectangle.


### -field right

X-coordinate of the lower-right corner of the rectangle.


### -field bottom

Y-coordinate of the lower-right corner of the rectangle.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

