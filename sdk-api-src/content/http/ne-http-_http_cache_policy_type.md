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

# _HTTP_CACHE_POLICY_TYPE enumeration


## -description


The 
<b>HTTP_CACHE_POLICY_TYPE</b> enumeration type defines available cache policies. It is used to restrict the values of the <b>Policy</b> member of the 
<a href="https://msdn.microsoft.com/91fcbf35-ef8b-4f70-9c31-3f741c0e2f6e">HTTP_CACHE_POLICY</a> structure, which in turn is used in the <i>pCachePolicy</i> parameter of the 
<a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a> function to specify how a response fragment is cached.


## -enum-fields




### -field HttpCachePolicyNocache

Do not cache this value at all.


### -field HttpCachePolicyUserInvalidates

Cache this value until the user provides a different one.


### -field HttpCachePolicyTimeToLive

Cache this value for a specified time and then remove it from the cache.


### -field HttpCachePolicyMaximum

Terminates the enumeration; not used to determine policy.


## -see-also




<a href="https://msdn.microsoft.com/91fcbf35-ef8b-4f70-9c31-3f741c0e2f6e">HTTP_CACHE_POLICY</a>



<a href="https://msdn.microsoft.com/caef2e93-39cd-4282-97d9-870f8236d8c4">HttpAddFragmentToCache</a>
 

 

