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

# _PROCESSOR_GROUP_INFO structure


## -description


Represents the number and affinity of processors in a processor group.


## -struct-fields




### -field MaximumProcessorCount

The maximum number of processors in the group.


### -field ActiveProcessorCount

The number of active processors in the group.


### -field Reserved

This member is reserved.


### -field ActiveProcessorMask

A bitmap that specifies the affinity for zero or more active processors within the group.


## -see-also




<a href="https://msdn.microsoft.com/3529ddef-04c5-4573-877d-c225da684e38">GROUP_RELATIONSHIP</a>
 

 

