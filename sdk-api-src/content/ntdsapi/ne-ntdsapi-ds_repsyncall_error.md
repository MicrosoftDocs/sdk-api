---
UID: NE:ntdsapi.__unnamed_enum_5
title: DS_REPSYNCALL_ERROR (ntdsapi.h)
description: The DS_REPSYNCALL_ERROR enumeration is used with the DS_REPSYNCALL_ERRINFO structure to indicate where in the replication process an error occurred.
helpviewer_keywords: ["DS_REPSYNCALL_ERROR","DS_REPSYNCALL_ERROR enumeration [Active Directory]","DS_REPSYNCALL_SERVER_UNREACHABLE","DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER","DS_REPSYNCALL_WIN32_ERROR_REPLICATING","ad.ds_repsyncall_error","ntdsapi/DS_REPSYNCALL_ERROR","ntdsapi/DS_REPSYNCALL_SERVER_UNREACHABLE","ntdsapi/DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER","ntdsapi/DS_REPSYNCALL_WIN32_ERROR_REPLICATING"]
old-location: ad\ds_repsyncall_error.htm
tech.root: ad
ms.assetid: 9c020046-ab52-4676-931e-12ce176e93fb
ms.date: 12/05/2018
ms.keywords: DS_REPSYNCALL_ERROR, DS_REPSYNCALL_ERROR enumeration [Active Directory], DS_REPSYNCALL_SERVER_UNREACHABLE, DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER, DS_REPSYNCALL_WIN32_ERROR_REPLICATING, ad.ds_repsyncall_error, ntdsapi/DS_REPSYNCALL_ERROR, ntdsapi/DS_REPSYNCALL_SERVER_UNREACHABLE, ntdsapi/DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER, ntdsapi/DS_REPSYNCALL_WIN32_ERROR_REPLICATING
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
req.typenames: DS_REPSYNCALL_ERROR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DS_REPSYNCALL_ERROR
 - ntdsapi/DS_REPSYNCALL_ERROR
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
 - DS_REPSYNCALL_ERROR
---

# DS_REPSYNCALL_ERROR enumeration


## -description

The <b>DS_REPSYNCALL_ERROR</b> enumeration is used with the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a> structure to indicate where in the replication process an error occurred.

## -enum-fields

### -field DS_REPSYNCALL_WIN32_ERROR_CONTACTING_SERVER:0

The server referred to by the <b>pszSvrId</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a> structure cannot be contacted.

### -field DS_REPSYNCALL_WIN32_ERROR_REPLICATING:1

An error occurred during replication of the server identified by the <b>pszSvrId</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a> structure.

### -field DS_REPSYNCALL_SERVER_UNREACHABLE:2

The server identified by the <b>pszSvrId</b> member of the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a> structure cannot be contacted.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasyncalla">DsReplicaSyncAll</a>
