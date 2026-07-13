---
UID: NF:ntdsapi.DsReplicaUpdateRefsA
title: DsReplicaUpdateRefsA function (ntdsapi.h)
description: Adds or removes a replication reference for a destination from a source naming context. (ANSI)
helpviewer_keywords: ["DS_REPUPD_ADD_REFERENCE", "DS_REPUPD_ASYNCHRONOUS_OPERATION", "DS_REPUPD_DELETE_REFERENCE", "DS_REPUPD_WRITEABLE", "DsReplicaUpdateRefsA", "ntdsapi/DsReplicaUpdateRefsA"]
old-location: ad\dsreplicaupdaterefs.htm
tech.root: ad
ms.assetid: 158c7e73-0e6c-4b71-a87f-2f60f3db91cb
ms.date: 12/05/2018
ms.keywords: DS_REPUPD_ADD_REFERENCE, DS_REPUPD_ASYNCHRONOUS_OPERATION, DS_REPUPD_DELETE_REFERENCE, DS_REPUPD_WRITEABLE, DsReplicaUpdateRefs, DsReplicaUpdateRefs function [Active Directory], DsReplicaUpdateRefsA, DsReplicaUpdateRefsW, _glines_dsreplicaupdaterefs, ad.dsreplicaupdaterefs, ntdsapi/DsReplicaUpdateRefs, ntdsapi/DsReplicaUpdateRefsA, ntdsapi/DsReplicaUpdateRefsW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaUpdateRefsW (Unicode) and DsReplicaUpdateRefsA (ANSI)
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
 - DsReplicaUpdateRefsA
 - ntdsapi/DsReplicaUpdateRefsA
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
 - DsReplicaUpdateRefs
 - DsReplicaUpdateRefsA
 - DsReplicaUpdateRefsW
---

# DsReplicaUpdateRefsA function


## -description

The <b>DsReplicaUpdateRefs</b> function adds or removes a replication reference for a destination from a source naming context.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param NameContext [in]

Pointer to a constant null-terminated string that specifies the distinguished name of the source naming context.

### -param DsaDest [in]

Pointer to a constant null-terminated string that specifies the transport-specific address of the destination directory system agent.

### -param pUuidDsaDest [in]

Pointer to a <b>UUID</b> value that contains the destination directory system agent.

### -param Options [in]

Contains a set of flags that provide additional data used to process the request. This can be zero or a combination of one or more of the following values.



#### DS_REPUPD_ADD_REFERENCE

A reference to the destination is added to the source server.



#### DS_REPUPD_ASYNCHRONOUS_OPERATION

The operation is performed asynchronously.



#### DS_REPUPD_DELETE_REFERENCE

A reference to the destination is removed from the source server.



#### DS_REPUPD_WRITEABLE

The reference to the replica  added or removed is writable. Otherwise, it is read-only.

## -returns

If the function succeeds,  <b>ERROR_SUCCESS</b> is returned.

If the function fails, the return value can be one of the following.

## -remarks

If both <b>DS_REPUPD_ADD_REFERENCE</b> and <b>DS_REPUPD_DELETE_REFERENCE</b> are set in the <i>Options</i> parameter, a reference to the destination is added if one does not already exist on the server. If a reference to the destination already exists, the reference is updated.





> [!NOTE]
> The ntdsapi.h header defines DsReplicaUpdateRefs as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicadela">DsReplicaDel</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasynca">DsReplicaSync</a>
