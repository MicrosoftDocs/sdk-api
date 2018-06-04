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

# DS_REPSYNCALL_ERROR enumeration


## -description


The <b>DS_REPSYNCALL_ERROR</b> enumeration is used with the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure to indicate where in the replication process an error occurred.


## -enum-fields




### -field DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER

The server referred to by the <b>pszSvrId</b> member of the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure cannot be contacted.


### -field DS_REPSYNCALL_WIN32_ERROR_REPLICATING

An error occurred during replication of the server identified by the <b>pszSvrId</b> member of the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure.


### -field DS_REPSYNCALL_SERVER_UNREACHABLE

The server identified by the <b>pszSvrId</b> member of the <a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure cannot be contacted.


## -see-also




<a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a>



<a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a>
 

 

