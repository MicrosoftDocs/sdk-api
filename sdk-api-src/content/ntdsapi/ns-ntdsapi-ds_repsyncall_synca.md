---
UID: NS:ntdsapi.__unnamed_struct_4
title: DS_REPSYNCALL_SYNCA (ntdsapi.h)
author: windows-sdk-content
description: The DS_REPSYNCALL_SYNC structure identifies a single replication operation performed between a source, and destination, server by the DsReplicaSyncAll function.
old-location: ad\ds_repsyncall_sync.htm
tech.root: ad
ms.assetid: 54a6695e-3493-428b-9e8d-7f781e7b3961
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDS_REPSYNCALL_SYNCA, DS_REPSYNCALL_SYNC, DS_REPSYNCALL_SYNC structure [Active Directory], DS_REPSYNCALL_SYNCA, DS_REPSYNCALL_SYNCW, PDS_REPSYNCALL_SYNC, PDS_REPSYNCALL_SYNC structure pointer [Active Directory], _glines_ds_repsyncall_sync, ad.ds__repsyncall__sync, ad.ds_repsyncall_sync, ntdsapi/DS_REPSYNCALL_SYNC, ntdsapi/DS_REPSYNCALL_SYNCA, ntdsapi/DS_REPSYNCALL_SYNCW, ntdsapi/PDS_REPSYNCALL_SYNC"
ms.topic: struct
f1_keywords: 
 - "ntdsapi/DS_REPSYNCALL_SYNC"
dev_langs:
 - c++
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_REPSYNCALL_SYNCW (Unicode) and DS_REPSYNCALL_SYNCA (ANSI)
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
 - DS_REPSYNCALL_SYNC
 - DS_REPSYNCALL_SYNCA
 - DS_REPSYNCALL_SYNCW
targetos: Windows
req.typenames: DS_REPSYNCALL_SYNCA, *PDS_REPSYNCALL_SYNCA
req.redist: 
ms.custom: 19H1
---

# DS_REPSYNCALL_SYNCA structure


## -description


The <b>DS_REPSYNCALL_SYNC</b> structure identifies a single replication operation performed between a source, and destination, server by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasyncalla">DsReplicaSyncAll</a> function.


## -struct-fields




### -field pszSrcId

Pointer to a null-terminated string that specifies the DNS GUID of the source server.


### -field pszDstId

Pointer to a null-terminated string that specifies the DNS GUID of the destination server.


### -field pszNC

 


### -field pguidSrc

 


### -field pguidDst

 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasyncalla">DsReplicaSyncAll</a>
 

 

