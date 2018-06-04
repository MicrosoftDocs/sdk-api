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

# tagCHUNKSTATE enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Specifies whether the current chunk is a text-type property or a value-type property.



## -enum-fields




### -field CHUNK_TEXT

The current chunk is a text-type property.


### -field CHUNK_VALUE

The current chunk is a value-type property.


### -field CHUNK_FILTER_OWNED_VALUE

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/4d4f3150-deec-40b6-a945-b4cea241db8d">IFilter::GetChunk</a>



<a href="https://msdn.microsoft.com/d63639a6-6729-44cd-8105-198a268ff2d6">IFilter::GetText</a>



<a href="https://msdn.microsoft.com/fb3e432d-3c8b-4567-9dc3-c35961f100ff">STAT_CHUNK</a>
 

 

