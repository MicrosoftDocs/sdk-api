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

# _HTTP_SERVICE_CONFIG_URLACL_KEY structure


## -description


The 
<b>HTTP_SERVICE_CONFIG_URLACL_KEY</b> structure is used to specify a particular reservation record in the URL namespace reservation store. It is a member of the 
<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a> and 
<a href="https://msdn.microsoft.com/298edd6c-c036-4e45-88f3-84917c8a76ea">HTTP_SERVICE_CONFIG_URLACL_QUERY</a> structures.


## -struct-fields




### -field pUrlPrefix

A pointer to the 
<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix string</a> that defines the portion of the URL namespace to which this reservation pertains.


## -see-also




<a href="https://msdn.microsoft.com/298edd6c-c036-4e45-88f3-84917c8a76ea">HTTP_SERVICE_CONFIG_URLACL_QUERY</a>



<a href="https://msdn.microsoft.com/92fc3f65-0153-4075-a61b-48a63c8e0ffe">HTTP_SERVICE_CONFIG_URLACL_SET</a>



<a href="https://msdn.microsoft.com/4f317bf6-ee6a-47a8-a531-78534217109d">UrlPrefix Strings</a>
 

 

