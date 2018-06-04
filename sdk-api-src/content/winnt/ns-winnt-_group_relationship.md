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

# _GROUP_RELATIONSHIP structure


## -description


Represents information about processor groups. This structure is used with the <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function.


## -struct-fields




### -field MaximumGroupCount

The maximum number of processor groups on the system.


### -field ActiveGroupCount

The number of active groups on the system. This member indicates the number of <a href="https://msdn.microsoft.com/6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03">PROCESSOR_GROUP_INFO</a> structures in the <b>GroupInfo</b> array.


### -field Reserved

This member is reserved.


### -field GroupInfo

An array of <a href="https://msdn.microsoft.com/6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03">PROCESSOR_GROUP_INFO</a> structures. Each structure represents the number and affinity of processors in an active group on the system.


## -see-also




<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/6ff9cc3c-34e7-4dc4-94cd-6ed278dfaa03">PROCESSOR_GROUP_INFO</a>



<a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

