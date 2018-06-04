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

# IDynamicRenderer::Draw


## -description



Draws the cached data to the specified device context.




## -parameters




### -param hDC [in]

 The handle of the device context on which to draw.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



You can use <b>IDynamicRenderer::Draw Method</b> for tasks such as double buffering.

<div class="alert"><b>Note</b>  Drawing cached data cannot be used on Microsoft&lt;entity type="reg"/&gt; Windows&lt;entity type="reg"/&gt; XP Tablet PC Edition 2005 systems.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>



<a href="https://msdn.microsoft.com/1b2435ee-4682-4499-aa5c-35201ab2ba95">IDynamicRenderer::DataCacheEnabled Property</a>



<a href="https://msdn.microsoft.com/d67a85e7-6dfc-4444-bb69-a46e1234d021">IDynamicRenderer::DrawingAttributes Property</a>



<a href="https://msdn.microsoft.com/691de815-a5be-4982-a59a-b904c070ede8">IDynamicRenderer::ReleaseCachedData Method</a>
 

 

