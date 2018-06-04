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

# IInkRectangle::get_Top


## -description



Gets or sets the top position of the <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle</a> object.



This property is read/write.


## -parameters


## -remarks



Note: A point is within an <a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a> if it lies on the <a href="https://msdn.microsoft.com/88f0d919-43d0-408f-97f8-1410b2833269">Left Property</a> or <b>Top Property</b> side or is within all four sides. A point on the <a href="https://msdn.microsoft.com/c31fd527-a6aa-4017-bc51-cedca42817f9">Right Property</a> or <a href="https://msdn.microsoft.com/9b388cdb-66b1-4386-a1aa-578f0d56c190">Bottom Property</a> side is considered outside the rectangle.

The default value of this property is 0.




## -see-also




<a href="https://msdn.microsoft.com/9b388cdb-66b1-4386-a1aa-578f0d56c190">Bottom Property</a>



<a href="tablet.iinkrectangle">IInkRectangle</a>



<a href="https://msdn.microsoft.com/78e6c29c-0f43-46a5-9d30-948de5f369c8">InkRectangle Class</a>



<a href="https://msdn.microsoft.com/88f0d919-43d0-408f-97f8-1410b2833269">Left Property</a>



<a href="https://msdn.microsoft.com/c31fd527-a6aa-4017-bc51-cedca42817f9">Right Property</a>
 

 

