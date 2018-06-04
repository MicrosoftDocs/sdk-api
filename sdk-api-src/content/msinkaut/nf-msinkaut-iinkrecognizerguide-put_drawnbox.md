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

# IInkRecognizerGuide::put_DrawnBox


## -description



Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.



This property is read/write.


## -parameters


## -remarks



The lines of the drawn box are visual cues that specify where writing can take place. The user normally writes within the boundaries of the lines.

Another box, the writing box, is the invisible box in which writing can actually take place. It is larger than the drawn box and provides a margin of error to users if they draw ink outside the lines of the drawn box. You can use the <a href="https://msdn.microsoft.com/60e37b92-22c2-4a71-a4d1-815226d804fa">WritingBox</a> property to set the writing box.

The writing box specifies the boundaries of the ink to the recognizer.The drawn box is drawn using ink space  units, relative to the top left of the writing box.




## -see-also




<a href="tablet.iinkrecognizerguide">IInkRecognizerGuide</a>



<a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide Class</a>



<a href="https://msdn.microsoft.com/60e37b92-22c2-4a71-a4d1-815226d804fa">WritingBox Property</a>
 

 

