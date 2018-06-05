---
UID: NE:ntdsapi.DS_REPSYNCALL_EVENT
title: DS_REPSYNCALL_EVENT
author: windows-sdk-content
description: The DS_REPSYNCALL_EVENT enumeration is used with the DS_REPSYNCALL_UPDATE structure to define which event the DS_REPSYNCALL_UPDATE structure represents.
old-location: ad\ds_repsyncall_event.htm
old-project: AD
ms.assetid: a732a906-0e26-45f6-b89c-58f2277057ba
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DS_REPSYNCALL_EVENT, DS_REPSYNCALL_EVENT enumeration [Active Directory], DS_REPSYNCALL_EVENT_ERROR, DS_REPSYNCALL_EVENT_FINISHED, DS_REPSYNCALL_EVENT_SYNC_COMPLETED, DS_REPSYNCALL_EVENT_SYNC_STARTED, ad.ds_repsyncall_event, ntdsapi/DS_REPSYNCALL_EVENT, ntdsapi/DS_REPSYNCALL_EVENT_ERROR, ntdsapi/DS_REPSYNCALL_EVENT_FINISHED, ntdsapi/DS_REPSYNCALL_EVENT_SYNC_COMPLETED, ntdsapi/DS_REPSYNCALL_EVENT_SYNC_STARTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DS_REPSYNCALL_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_REPSYNCALL_EVENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: Any level
req.product: Rights Management Services client 1.0 or later
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
 

 

