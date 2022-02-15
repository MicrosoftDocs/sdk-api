---
UID: NE:ntdsapi._DS_REPL_OP_TYPE
title: DS_REPL_OP_TYPE (ntdsapi.h)
description: Used to indicate the type of replication operation that a given entry in the replication queue represents.
helpviewer_keywords: ["DS_REPL_OP_TYPE","DS_REPL_OP_TYPE enumeration [Active Directory]","DS_REPL_OP_TYPE_ADD","DS_REPL_OP_TYPE_DELETE","DS_REPL_OP_TYPE_MODIFY","DS_REPL_OP_TYPE_SYNC","DS_REPL_OP_TYPE_UPDATE_REFS","_glines_ds_repl_op_type","ad.ds__repl__op__type","ad.ds_repl_op_type","ntdsapi/DS_REPL_OP_TYPE","ntdsapi/DS_REPL_OP_TYPE_ADD","ntdsapi/DS_REPL_OP_TYPE_DELETE","ntdsapi/DS_REPL_OP_TYPE_MODIFY","ntdsapi/DS_REPL_OP_TYPE_SYNC","ntdsapi/DS_REPL_OP_TYPE_UPDATE_REFS"]
old-location: ad\ds_repl_op_type.htm
tech.root: ad
ms.assetid: 81d9f464-90f4-405c-b014-0a61f5a5b816
ms.date: 12/05/2018
ms.keywords: DS_REPL_OP_TYPE, DS_REPL_OP_TYPE enumeration [Active Directory], DS_REPL_OP_TYPE_ADD, DS_REPL_OP_TYPE_DELETE, DS_REPL_OP_TYPE_MODIFY, DS_REPL_OP_TYPE_SYNC, DS_REPL_OP_TYPE_UPDATE_REFS, _glines_ds_repl_op_type, ad.ds__repl__op__type, ad.ds_repl_op_type, ntdsapi/DS_REPL_OP_TYPE, ntdsapi/DS_REPL_OP_TYPE_ADD, ntdsapi/DS_REPL_OP_TYPE_DELETE, ntdsapi/DS_REPL_OP_TYPE_MODIFY, ntdsapi/DS_REPL_OP_TYPE_SYNC, ntdsapi/DS_REPL_OP_TYPE_UPDATE_REFS
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
req.typenames: DS_REPL_OP_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_OP_TYPE
 - ntdsapi/_DS_REPL_OP_TYPE
 - DS_REPL_OP_TYPE
 - ntdsapi/DS_REPL_OP_TYPE
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
 - DS_REPL_OP_TYPE
---

# DS_REPL_OP_TYPE enumeration


## -description

The <b>DS_REPL_OP_TYPE</b> enumeration type is used to indicate the type of replication operation that a given entry in the replication queue represents.

## -enum-fields

### -field DS_REPL_OP_TYPE_SYNC:0

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

<a href="/windows/desktop/AD/enumerations-in-active-directory-domain-services">Active Directory Enumerations</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>
