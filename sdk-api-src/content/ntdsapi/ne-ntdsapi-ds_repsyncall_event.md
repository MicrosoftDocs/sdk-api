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

# DS_REPSYNCALL_EVENT enumeration


## -description


The <b>DS_REPSYNCALL_EVENT</b> enumeration is used with the <a href="https://msdn.microsoft.com/3b0005cb-0fb6-492c-89e5-8a18a88f881b">DS_REPSYNCALL_UPDATE</a> structure to define which event the <b>DS_REPSYNCALL_UPDATE</b> structure represents.


## -enum-fields




### -field DS_REPSYNCALL_EVENT_ERROR

An error occurred. Error data is stored in the <b>pErrInfo</b> member of the <a href="https://msdn.microsoft.com/3b0005cb-0fb6-492c-89e5-8a18a88f881b">DS_REPSYNCALL_UPDATE</a> structure.


### -field DS_REPSYNCALL_EVENT_SYNC_STARTED

Synchronization of two servers has started. Both the <b>pErrInfo</b> and <b>pSync</b> members of the <a href="https://msdn.microsoft.com/3b0005cb-0fb6-492c-89e5-8a18a88f881b">DS_REPSYNCALL_UPDATE</a> structure are <b>NULL</b>.


### -field DS_REPSYNCALL_EVENT_SYNC_COMPLETED

Synchronization of two servers has just finished. The servers involved in the synchronization are identified by the <b>pSync</b> member of the <a href="https://msdn.microsoft.com/3b0005cb-0fb6-492c-89e5-8a18a88f881b">DS_REPSYNCALL_UPDATE</a> structure. The <b>pErrInfo</b> member of the <b>DS_REPSYNCALL_UPDATE</b> structure is <b>NULL</b>.


### -field DS_REPSYNCALL_EVENT_FINISHED

Execution of <a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a> is complete. Both the <b>pErrInfo</b> and <b>pSync</b> members of the <a href="https://msdn.microsoft.com/3b0005cb-0fb6-492c-89e5-8a18a88f881b">DS_REPSYNCALL_UPDATE</a> structure are <b>NULL</b>. The return value of the callback function is ignored.


## -see-also




<a href="https://msdn.microsoft.com/3b0005cb-0fb6-492c-89e5-8a18a88f881b">DS_REPSYNCALL_UPDATE</a>
 

 

