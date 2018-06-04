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

# _HTTP_SERVICE_BINDING_BASE structure


## -description


The <b>HTTP_SERVICE_BINDING_BASE</b> structure is a placeholder for the <a href="https://msdn.microsoft.com/bad1a042-fda8-4a2a-a8c1-26ed1f87c442">HTTP_SERVICE_BINDING_A</a> structure and the <a href="https://msdn.microsoft.com/0d840097-82d3-4ee3-b0d9-bcac4cf3e935">HTTP_SERVICE_BINDING_W</a> structure.


## -struct-fields




### -field Type

Pointer to an <a href="https://msdn.microsoft.com/8de36795-c99d-46ce-b9e4-a933de7d4c5c">HTTP_SERVICE_BINDING_TYPE</a> value that indicates whether the data is in ASCII or Unicode.


## -remarks



<div class="alert"><b>Note</b>  <p class="note">The first member of both the  <a href="https://msdn.microsoft.com/bad1a042-fda8-4a2a-a8c1-26ed1f87c442">HTTP_SERVICE_BINDING_A</a> structure and the <a href="https://msdn.microsoft.com/0d840097-82d3-4ee3-b0d9-bcac4cf3e935">HTTP_SERVICE_BINDING_W</a> structure is a <b>HTTP_SERVICE_BINDING_BASE</b> structure.  Therefore, an array of either of the first two structures can be indicated by a pointer to a <b>HTTP_SERVICE_BINDING_BASE</b> structure.

<p class="note">The <b>ServiceNames</b> member of the <a href="https://msdn.microsoft.com/60428e66-9c08-418b-99e1-6824c638f2be">HTTP_CHANNEL_BIND_INFO</a> structure is cast to a  pointer to a <b>HTTP_SERVICE_BINDING_BASE</b> structure for this purpose.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/60428e66-9c08-418b-99e1-6824c638f2be">HTTP_CHANNEL_BIND_INFO</a>



<a href="https://msdn.microsoft.com/bad1a042-fda8-4a2a-a8c1-26ed1f87c442">HTTP_SERVICE_BINDING_A</a>



<a href="https://msdn.microsoft.com/8de36795-c99d-46ce-b9e4-a933de7d4c5c">HTTP_SERVICE_BINDING_TYPE</a>



<a href="https://msdn.microsoft.com/0d840097-82d3-4ee3-b0d9-bcac4cf3e935">HTTP_SERVICE_BINDING_W</a>
 

 

