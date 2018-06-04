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

# GET_OPERATION_CONTEXT_PARAMS structure


## -description


Represents context parameters that are used as input for the <a href="https://msdn.microsoft.com/BCB58D8A-5FF6-46BD-8144-919C6DB44593">CLUSCTL_RESOURCE_GET_OPERATION_CONTEXT</a> control code.


## -struct-fields




### -field Size

The size of this structure, in bytes.


### -field Version

The version of this structure.


### -field Type

A  <a href="https://msdn.microsoft.com/8C074E15-4060-4AC7-BB59-959854102EE0">RESDLL_CONTEXT_OPERATION_TYPE</a> enumeration value that specifies the context operation type.


### -field Priority

TBD


## -see-also




<a href="https://msdn.microsoft.com/9ab4b974-28b5-4f33-a7c4-b9b2472059aa">Resource DLL Structures</a>
 

 

