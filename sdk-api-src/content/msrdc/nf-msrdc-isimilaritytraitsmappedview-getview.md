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

# ISimilarityTraitsMappedView::GetView


## -description


Returns the beginning and ending addresses for the mapped view of a similarity traits table file.


## -parameters




### -param mappedPageBegin [out]

Pointer to a location that receives the start of the data that is mapped for this view.


### -param mappedPageEnd [out]

Pointer to a location that receives the end of the data that is mapped for this view, plus one.


## -returns



This method does not return a value.




## -remarks



If there is no mapped view, then <code>*mappedPageBegin</code> must be set to zero. Otherwise, <code>*mappedPageBegin</code> is set to a valid pointer, and <code>*mappedPageBegin - *mappedPageEnd</code> equals the size, in bytes, of the mapped area.




## -see-also




<a href="https://msdn.microsoft.com/48d6d4a0-fbf1-476a-b30f-83176c51cb48">ISimilarityTraitsMappedView</a>
 

 

