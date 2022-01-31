---
UID: NE:ntdsapi.__unnamed_enum_6
title: DS_REPSYNCALL_EVENT (ntdsapi.h)
description: The DS_REPSYNCALL_EVENT enumeration is used with the DS_REPSYNCALL_UPDATE structure to define which event the DS_REPSYNCALL_UPDATE structure represents.
helpviewer_keywords: ["DS_REPSYNCALL_EVENT","DS_REPSYNCALL_EVENT enumeration [Active Directory]","DS_REPSYNCALL_EVENT_ERROR","DS_REPSYNCALL_EVENT_FINISHED","DS_REPSYNCALL_EVENT_SYNC_COMPLETED","DS_REPSYNCALL_EVENT_SYNC_STARTED","ad.ds_repsyncall_event","ntdsapi/DS_REPSYNCALL_EVENT","ntdsapi/DS_REPSYNCALL_EVENT_ERROR","ntdsapi/DS_REPSYNCALL_EVENT_FINISHED","ntdsapi/DS_REPSYNCALL_EVENT_SYNC_COMPLETED","ntdsapi/DS_REPSYNCALL_EVENT_SYNC_STARTED"]
old-location: ad\ds_repsyncall_event.htm
tech.root: ad
ms.assetid: a732a906-0e26-45f6-b89c-58f2277057ba
ms.date: 12/05/2018
ms.keywords: DS_REPSYNCALL_EVENT, DS_REPSYNCALL_EVENT enumeration [Active Directory], DS_REPSYNCALL_EVENT_ERROR, DS_REPSYNCALL_EVENT_FINISHED, DS_REPSYNCALL_EVENT_SYNC_COMPLETED, DS_REPSYNCALL_EVENT_SYNC_STARTED, ad.ds_repsyncall_event, ntdsapi/DS_REPSYNCALL_EVENT, ntdsapi/DS_REPSYNCALL_EVENT_ERROR, ntdsapi/DS_REPSYNCALL_EVENT_FINISHED, ntdsapi/DS_REPSYNCALL_EVENT_SYNC_COMPLETED, ntdsapi/DS_REPSYNCALL_EVENT_SYNC_STARTED
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DS_REPSYNCALL_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DS_REPSYNCALL_EVENT
 - ntdsapi/DS_REPSYNCALL_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPSYNCALL_EVENT
---

# DS_REPSYNCALL_EVENT enumeration


## -description

The <b>DS_REPSYNCALL_EVENT</b> enumeration is used with the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a> structure to define which event the <b>DS_REPSYNCALL_UPDATE</b> structure represents.

## -enum-fields

### -field DS_REPSYNCALL_EVENT_ERROR:0

An error occurred. Error data is stored in the <b>pErrInfo</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a> structure.

### -field DS_REPSYNCALL_EVENT_SYNC_STARTED:1

Synchronization of two servers has started. Both the <b>pErrInfo</b> and <b>pSync</b> members of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a> structure are <b>NULL</b>.

### -field DS_REPSYNCALL_EVENT_SYNC_COMPLETED:2

Synchronization of two servers has just finished. The servers involved in the synchronization are identified by the <b>pSync</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a> structure. The <b>pErrInfo</b> member of the <b>DS_REPSYNCALL_UPDATE</b> structure is <b>NULL</b>.

### -field DS_REPSYNCALL_EVENT_FINISHED:3

Execution of <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasyncalla">DsReplicaSyncAll</a> is complete. Both the <b>pErrInfo</b> and <b>pSync</b> members of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a> structure are <b>NULL</b>. The return value of the callback function is ignored.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_updatea">DS_REPSYNCALL_UPDATE</a>
