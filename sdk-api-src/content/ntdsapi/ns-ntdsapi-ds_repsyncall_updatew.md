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

# DS_REPSYNCALL_UPDATEW structure


## -description


The <b>DS_REPSYNCALL_UPDATE</b> structure contains status data about the replication performed by the 
<a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a> function. The <b>DsReplicaSyncAll</b> function passes this structure to a callback function in its <i>pFnCallBack</i> parameter. For more information about the callback function, see 
<a href="https://msdn.microsoft.com/b5243a07-b058-4384-aafc-bf80078d904b">SyncUpdateProc</a>.


## -struct-fields




### -field event

Contains a <a href="https://msdn.microsoft.com/a732a906-0e26-45f6-b89c-58f2277057ba">DS_REPSYNCALL_EVENT</a> value that describes the event which the <b>DS_REPSYNCALL_UPDATE</b> structure represents.


### -field pErrInfo

Pointer to a 
<a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a> structure that contains error data about the replication performed by the <a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a> function.


### -field pSync

Pointer to a 
<a href="https://msdn.microsoft.com/54a6695e-3493-428b-9e8d-7f781e7b3961">DS_REPSYNCALL_SYNC</a> structure that identifies the source and destination servers that have either initiated or finished synchronization.


## -see-also




<a href="https://msdn.microsoft.com/70af4e3e-1f0e-49c5-b8c6-5e89114ed4ea">DS_REPSYNCALL_ERRINFO</a>



<a href="https://msdn.microsoft.com/a732a906-0e26-45f6-b89c-58f2277057ba">DS_REPSYNCALL_EVENT</a>



<a href="https://msdn.microsoft.com/54a6695e-3493-428b-9e8d-7f781e7b3961">DS_REPSYNCALL_SYNC</a>



<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>



<a href="https://msdn.microsoft.com/2608adde-4f18-4048-a96f-d736ff09cd4b">DsReplicaSyncAll</a>



<a href="https://msdn.microsoft.com/b5243a07-b058-4384-aafc-bf80078d904b">SyncUpdateProc</a>
 

 

