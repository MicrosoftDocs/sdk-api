---
UID: NS:ntdsapi.DS_REPSYNCALL_UPDATEA
title: DS_REPSYNCALL_UPDATEA
author: windows-sdk-content
description: The DS_REPSYNCALL_UPDATE structure contains status data about the replication performed by the DsReplicaSyncAll function.
old-location: ad\ds_repsyncall_update.htm
tech.root: AD
ms.assetid: 3b0005cb-0fb6-492c-89e5-8a18a88f881b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDS_REPSYNCALL_UPDATEA, DS_REPSYNCALL_UPDATE, DS_REPSYNCALL_UPDATE structure [Active Directory], DS_REPSYNCALL_UPDATEA, DS_REPSYNCALL_UPDATEW, PDS_REPSYNCALL_UPDATE, PDS_REPSYNCALL_UPDATE structure pointer [Active Directory], _glines_ds_repsyncall_update, ad.ds__repsyncall__update, ad.ds_repsyncall_update, ntdsapi/DS_REPSYNCALL_UPDATE, ntdsapi/DS_REPSYNCALL_UPDATEA, ntdsapi/DS_REPSYNCALL_UPDATEW, ntdsapi/PDS_REPSYNCALL_UPDATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_REPSYNCALL_UPDATEW (Unicode) and DS_REPSYNCALL_UPDATEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPSYNCALL_UPDATE
 - DS_REPSYNCALL_UPDATEA
 - DS_REPSYNCALL_UPDATEW
product: Windows
targetos: Windows
req.typenames: DS_REPSYNCALL_UPDATEA, *PDS_REPSYNCALL_UPDATEA
req.redist: 
---

# DS_REPSYNCALL_UPDATEA structure


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
 

 

