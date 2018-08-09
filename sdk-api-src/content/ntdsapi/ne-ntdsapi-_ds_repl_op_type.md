---
UID: NE:ntdsapi._DS_REPL_OP_TYPE
title: "_DS_REPL_OP_TYPE"
author: windows-sdk-content
description: Used to indicate the type of replication operation that a given entry in the replication queue represents.
old-location: ad\ds_repl_op_type.htm
old-project: ad
ms.assetid: 81d9f464-90f4-405c-b014-0a61f5a5b816
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DS_REPL_OP_TYPE, DS_REPL_OP_TYPE enumeration [Active Directory], DS_REPL_OP_TYPE_ADD, DS_REPL_OP_TYPE_DELETE, DS_REPL_OP_TYPE_MODIFY, DS_REPL_OP_TYPE_SYNC, DS_REPL_OP_TYPE_UPDATE_REFS, _DS_REPL_OP_TYPE, _glines_ds_repl_op_type, ad.ds__repl__op__type, ad.ds_repl_op_type, ntdsapi/DS_REPL_OP_TYPE, ntdsapi/DS_REPL_OP_TYPE_ADD, ntdsapi/DS_REPL_OP_TYPE_DELETE, ntdsapi/DS_REPL_OP_TYPE_MODIFY, ntdsapi/DS_REPL_OP_TYPE_SYNC, ntdsapi/DS_REPL_OP_TYPE_UPDATE_REFS
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
req.typenames: DS_REPL_OP_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_OP_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: Any level
req.product: Rights Management Services client 1.0 or later
---

# _DS_REPL_OP_TYPE enumeration


## -description


The <b>DS_REPL_OP_TYPE</b> enumeration type is used to indicate the type of replication operation that a given entry in the replication queue represents.


## -enum-fields




### -field DS_REPL_OP_TYPE_SYNC

Indicates an inbound replication over an existing replication agreement from a direct replication partner.


### -field DS_REPL_OP_TYPE_ADD

Indicates the addition of a replication agreement for a new direct replication partner.


### -field DS_REPL_OP_TYPE_DELETE

Indicates the removal of a replication agreement for an existing direct replication partner.


### -field DS_REPL_OP_TYPE_MODIFY

Indicates the modification of a replication agreement for an existing direct replication partner.


### -field DS_REPL_OP_TYPE_UPDATE_REFS

Indicates the addition, deletion, or update of outbound change notification data for a direct replication partner.


## -see-also




<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Active Directory Enumerations</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

