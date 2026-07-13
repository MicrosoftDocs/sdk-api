---
UID: NF:ntdsapi.DsReplicaDelW
title: DsReplicaDelW function (ntdsapi.h)
description: Removes a replication source reference from a destination naming context (NC). (Unicode)
helpviewer_keywords: ["DS_REPDEL_ASYNCHRONOUS_OPERATION", "DS_REPDEL_IGNORE_ERRORS", "DS_REPDEL_INTERSITE_MESSAGING", "DS_REPDEL_LOCAL_ONLY", "DS_REPDEL_NO_SOURCE", "DS_REPDEL_REF_OK", "DS_REPDEL_WRITEABLE", "DsReplicaDel", "DsReplicaDel function [Active Directory]", "DsReplicaDelW", "_glines_dsreplicadel", "ad.dsreplicadel", "ntdsapi/DsReplicaDel", "ntdsapi/DsReplicaDelW"]
old-location: ad\dsreplicadel.htm
tech.root: ad
ms.assetid: 68c767c4-bbb6-477b-8ffb-94f3ae235375
ms.date: 12/05/2018
ms.keywords: DS_REPDEL_ASYNCHRONOUS_OPERATION, DS_REPDEL_IGNORE_ERRORS, DS_REPDEL_INTERSITE_MESSAGING, DS_REPDEL_LOCAL_ONLY, DS_REPDEL_NO_SOURCE, DS_REPDEL_REF_OK, DS_REPDEL_WRITEABLE, DsReplicaDel, DsReplicaDel function [Active Directory], DsReplicaDelA, DsReplicaDelW, _glines_dsreplicadel, ad.dsreplicadel, ntdsapi/DsReplicaDel, ntdsapi/DsReplicaDelA, ntdsapi/DsReplicaDelW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaDelW (Unicode) and DsReplicaDelA (ANSI)
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
 - DsReplicaDelW
 - ntdsapi/DsReplicaDelW
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
 - DsReplicaDel
 - DsReplicaDelA
 - DsReplicaDelW
---

# DsReplicaDelW function


## -description

The <b>DsReplicaDel</b> function removes a replication source reference from a destination naming context (NC).

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param NameContext [in]

Pointer to a constant null-terminated string that specifies the distinguished name (DN) of the destination NC from which to remove the replica. The destination NC record must exist locally as either an object, instantiated or not, or a reference phantom, for example, a phantom with a GUID.

### -param DsaSrc [in]

Pointer to a constant null-terminated Unicode string that specifies the transport-specific address of the source directory system agent (DSA). This source server is identified by a string name, not by its <b>UUID</b>. A string name appropriate for <i>DsaSrc</i> is usually a DNS name that is based on a <b>GUID</b>, where the <b>GUID</b> part of the name is the <b>GUID</b> of the nTDSDSA object for the source server.

### -param Options [in]

Passes additional data used to process the request. This parameter can be a combination of the following values.



#### DS_REPDEL_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.



#### DS_REPDEL_IGNORE_ERRORS

Ignores any error generated from contacting the source to instruct it to remove this NC from its list of servers to which it replicates.



#### DS_REPDEL_INTERSITE_MESSAGING

Signifies the replica is mail-based rather than synchronized using native directory service RPC.



#### DS_REPDEL_LOCAL_ONLY

Does not contact the source to tell it to remove this NC from its list of servers to which it replicates. If this flag is not set and the link is based in RPC, the source is contacted.



#### DS_REPDEL_NO_SOURCE

Deletes all the objects in the NC. This option is valid only for read-only NCs with no source.



#### DS_REPDEL_REF_OK

Allows deletion of a read-only replica even if it sources other read-only replicas.



#### DS_REPDEL_WRITEABLE

Signifies that the replica deleted can be written to.


##### - Options.DS_REPDEL_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.


##### - Options.DS_REPDEL_IGNORE_ERRORS

Ignores any error generated from contacting the source to instruct it to remove this NC from its list of servers to which it replicates.


##### - Options.DS_REPDEL_INTERSITE_MESSAGING

Signifies the replica is mail-based rather than synchronized using native directory service RPC.


##### - Options.DS_REPDEL_LOCAL_ONLY

Does not contact the source to tell it to remove this NC from its list of servers to which it replicates. If this flag is not set and the link is based in RPC, the source is contacted.


##### - Options.DS_REPDEL_NO_SOURCE

Deletes all the objects in the NC. This option is valid only for read-only NCs with no source.


##### - Options.DS_REPDEL_REF_OK

Allows deletion of a read-only replica even if it sources other read-only replicas.


##### - Options.DS_REPDEL_WRITEABLE

Signifies that the replica deleted can be written to.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a standard Win32 API error or <b>ERROR_INVALID_PARAMETER</b> if a parameter is invalid.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaadda">DsReplicaAdd</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicamodifya">DsReplicaModify</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasynca">DsReplicaSync</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa">DsReplicaUpdateRefs</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsReplicaDel as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
