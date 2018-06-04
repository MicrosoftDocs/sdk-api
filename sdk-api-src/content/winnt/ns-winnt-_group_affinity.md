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

# _GROUP_AFFINITY structure


## -description


Represents a processor group-specific affinity, such as the affinity of a thread.


## -struct-fields




### -field Mask

A bitmap that specifies the affinity for zero or more processors within the specified group.


### -field Group

The processor group number.


### -field Reserved

This member is reserved.


## -see-also




<a href="https://msdn.microsoft.com/f8fe521b-02d6-4c58-8ef8-653280add111">CACHE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/a4e4c994-c4af-4b4f-8684-6037bcba35a9">NUMA_NODE_RELATIONSHIP</a>



<a href="https://msdn.microsoft.com/1efda80d-cf5b-4312-801a-ea3585b152ac">PROCESSOR_RELATIONSHIP</a>
 

 

