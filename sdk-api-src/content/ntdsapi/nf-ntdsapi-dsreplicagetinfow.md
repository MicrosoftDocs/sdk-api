---
UID: NF:ntdsapi.DsReplicaGetInfoW
title: DsReplicaGetInfoW function (ntdsapi.h)
description: Retrieves replication state data from the directory service.
helpviewer_keywords: ["DS_REPL_INFO_CURSORS_FOR_NC","DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES","DS_REPL_INFO_KCC_DSA_LINK_FAILURES","DS_REPL_INFO_METADATA_FOR_OBJ","DS_REPL_INFO_NEIGHBORS","DS_REPL_INFO_PENDING_OPS","DsReplicaGetInfo","DsReplicaGetInfo function [Active Directory]","DsReplicaGetInfoW","_glines_dsreplicagetinfo","ad.dsreplicagetinfo","ntdsapi/DsReplicaGetInfo","ntdsapi/DsReplicaGetInfoW"]
old-location: ad\dsreplicagetinfo.htm
tech.root: ad
ms.assetid: b7ab22fe-ed92-4213-9b66-2dd5526286fa
ms.date: 12/05/2018
ms.keywords: DS_REPL_INFO_CURSORS_FOR_NC, DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, DS_REPL_INFO_KCC_DSA_LINK_FAILURES, DS_REPL_INFO_METADATA_FOR_OBJ, DS_REPL_INFO_NEIGHBORS, DS_REPL_INFO_PENDING_OPS, DsReplicaGetInfo, DsReplicaGetInfo function [Active Directory], DsReplicaGetInfoW, _glines_dsreplicagetinfo, ad.dsreplicagetinfo, ntdsapi/DsReplicaGetInfo, ntdsapi/DsReplicaGetInfoW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaGetInfoW (Unicode)
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
 - DsReplicaGetInfoW
 - ntdsapi/DsReplicaGetInfoW
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
 - DsReplicaGetInfo
 - DsReplicaGetInfoW
---

# DsReplicaGetInfoW function


## -description

The <b>DsReplicaGetInfo</b> function retrieves replication state data from the directory service.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param InfoType [in]

Contains one of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a> values that specifies the type of replication data to retrieve. This value also determines which type of structure is returned in <i>ppInfo</i>.

Only the following values are supported for this function. If other data types are required, the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function must be used.

<a id="DS_REPL_INFO_NEIGHBORS"></a>
<a id="ds_repl_info_neighbors"></a>


#### DS_REPL_INFO_NEIGHBORS

<a id="DS_REPL_INFO_CURSORS_FOR_NC"></a>
<a id="ds_repl_info_cursors_for_nc"></a>


#### DS_REPL_INFO_CURSORS_FOR_NC

<a id="DS_REPL_INFO_METADATA_FOR_OBJ"></a>
<a id="ds_repl_info_metadata_for_obj"></a>


#### DS_REPL_INFO_METADATA_FOR_OBJ

<a id="DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES"></a>
<a id="ds_repl_info_kcc_dsa_connect_failures"></a>


#### DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES

<a id="DS_REPL_INFO_KCC_DSA_LINK_FAILURES"></a>
<a id="ds_repl_info_kcc_dsa_link_failures"></a>


#### DS_REPL_INFO_KCC_DSA_LINK_FAILURES

<a id="DS_REPL_INFO_PENDING_OPS"></a>
<a id="ds_repl_info_pending_ops"></a>


#### DS_REPL_INFO_PENDING_OPS

### -param pszObject [in, optional]

Pointer to a constant null-terminated Unicode string that identifies the object to retrieve replication data for. The meaning of this parameter depends on the value of the <i>InfoType</i> parameter. The following are possible value codes.



#### DS_REPL_INFO_NEIGHBORS

<i>pszObject</i> identifies the naming context for which replication neighbors are requested.



#### DS_REPL_INFO_CURSORS_FOR_NC

<i>pszObject</i> identifies the naming context for which replication cursors are requested.



#### DS_REPL_INFO_METADATA_FOR_OBJ

<i>pszObject</i> identifies the object for which replication metadata is requested.



#### DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES

<i>pszObject</i> must be <b>NULL</b>.



#### DS_REPL_INFO_KCC_DSA_LINK_FAILURES

<i>pszObject</i> must be <b>NULL</b>.



#### DS_REPL_INFO_PENDING_OPS

<i>pszObject</i> must be <b>NULL</b>.

### -param puuidForSourceDsaObjGuid [in, optional]

Pointer to a <b>GUID</b> value that identifies a specific replication source. If this parameter is not <b>NULL</b> and the <i>InfoType</i> parameter contains <b>DS_REPL_INFO_NEIGHBORS</b>, only neighbor data for the source corresponding to the nTDSDSA object with the given <b>objectGuid</b> in the directory is returned. This parameter is ignored if <b>NULL</b> or if the <i>InfoType</i> parameter is anything other than <b>DS_REPL_INFO_NEIGHBORS</b>.

### -param ppInfo [out]

Address of a structure pointer that receives the requested data. The value of the <i>InfoType</i> parameter determines the format of this structure. For more information and list of possible <i>InfoType</i> values and the corresponding structure types, see <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a>.

The caller must free this memory when it is no longer required by calling <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicafreeinfo">DsReplicaFreeInfo</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error otherwise.
      The following are possible error codes.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicafreeinfo">DsReplicaFreeInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>