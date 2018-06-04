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

# IInkRecognizerGuide::get_WritingBox


## -description



Gets or sets the invisible writing area of the recognition guide in which writing can actually take place.



This property is read/write.


## -parameters


## -remarks



The writing box provides a margin of error to users who write outside the drawn box-the lines that are physically drawn on the tablet screen within which users write. You can use the <a href="https://msdn.microsoft.com/f99095e1-8e7f-47eb-9234-70f651ebf793">DrawnBox</a> property to set the drawn box.




## -see-also




<a href="https://msdn.microsoft.com/f99095e1-8e7f-47eb-9234-70f651ebf793">DrawnBox Property</a>



<a href="tablet.iinkrecognizerguide">IInkRecognizerGuide</a>



<a href="https://msdn.microsoft.com/c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7">InkRecognizerGuide Class</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>
 

 

