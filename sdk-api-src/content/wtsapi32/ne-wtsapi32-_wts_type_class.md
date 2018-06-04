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

# _WTS_TYPE_CLASS enumeration


## -description


Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.


## -enum-fields




### -field WTSTypeProcessInfoLevel0

The buffer contains one or more <a href="https://msdn.microsoft.com/5df01ad8-71fd-4831-8eba-1d6cabd61348">WTS_PROCESS_INFO</a> structures.


### -field WTSTypeProcessInfoLevel1

The buffer contains one or more <a href="https://msdn.microsoft.com/a678d249-4943-4d2b-9cea-87ce20177c75">WTS_PROCESS_INFO_EX</a> structures.


### -field WTSTypeSessionInfoLevel1

The buffer contains one or more <a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/1c325174-ec08-4bbb-8e91-1a3cc9256110">WTSFreeMemory</a>



<a href="https://msdn.microsoft.com/d84a4fe3-a829-4cf3-b217-157391d0c495">WTSFreeMemoryEx</a>
 

 

