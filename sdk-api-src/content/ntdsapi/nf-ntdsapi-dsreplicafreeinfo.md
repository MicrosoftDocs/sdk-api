---
UID: NF:ntdsapi.DsReplicaFreeInfo
title: DsReplicaFreeInfo function (ntdsapi.h)
description: Frees the replication state data structure allocated by the DsReplicaGetInfo or DsReplicaGetInfo2 functions.
helpviewer_keywords: ["DsReplicaFreeInfo","DsReplicaFreeInfo function [Active Directory]","ad.dsreplicafreeinfo","ntdsapi/DsReplicaFreeInfo"]
old-location: ad\dsreplicafreeinfo.htm
tech.root: ad
ms.assetid: 32ce378e-a178-4970-b3bd-3887866e97af
ms.date: 12/05/2018
ms.keywords: DsReplicaFreeInfo, DsReplicaFreeInfo function [Active Directory], ad.dsreplicafreeinfo, ntdsapi/DsReplicaFreeInfo
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
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsReplicaFreeInfo
 - ntdsapi/DsReplicaFreeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsReplicaFreeInfo
---

# DsReplicaFreeInfo function


## -description

The <b>DsReplicaFreeInfo</b> function frees the replication state data structure allocated by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> or <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions.

## -parameters

### -param InfoType [in]

Contains one of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a> values that specifies the type of replication data structure  contained in <i>pInfo</i>. This must be the same value passed to the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> or <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function when the structure was allocated.

### -param pInfo [in]

Pointer to the replication data structure allocated by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> or <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>