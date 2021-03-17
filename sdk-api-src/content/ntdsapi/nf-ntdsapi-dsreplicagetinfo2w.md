---
UID: NF:ntdsapi.DsReplicaGetInfo2W
title: DsReplicaGetInfo2W function (ntdsapi.h)
description: Retrieves replication state data from the directory service. This function allows paging of results in cases where there are more than 1000 entries to retrieve.
helpviewer_keywords: ["DS_REPL_INFO_CURSORS_2_FOR_NC","DS_REPL_INFO_CURSORS_3_FOR_NC","DS_REPL_INFO_CURSORS_FOR_NC","DS_REPL_INFO_FLAG_IMPROVE_LINKED_ATTRS","DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES","DS_REPL_INFO_KCC_DSA_LINK_FAILURES","DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE","DS_REPL_INFO_METADATA_2_FOR_OBJ","DS_REPL_INFO_METADATA_FOR_ATTR_VALUE","DS_REPL_INFO_METADATA_FOR_OBJ","DS_REPL_INFO_NEIGHBORS","DS_REPL_INFO_PENDING_OPS","DsReplicaGetInfo2","DsReplicaGetInfo2 function [Active Directory]","DsReplicaGetInfo2W","ad.dsreplicagetinfo2","ntdsapi/DsReplicaGetInfo2","ntdsapi/DsReplicaGetInfo2W"]
old-location: ad\dsreplicagetinfo2.htm
tech.root: ad
ms.assetid: 5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d
ms.date: 12/05/2018
ms.keywords: DS_REPL_INFO_CURSORS_2_FOR_NC, DS_REPL_INFO_CURSORS_3_FOR_NC, DS_REPL_INFO_CURSORS_FOR_NC, DS_REPL_INFO_FLAG_IMPROVE_LINKED_ATTRS, DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, DS_REPL_INFO_KCC_DSA_LINK_FAILURES, DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE, DS_REPL_INFO_METADATA_2_FOR_OBJ, DS_REPL_INFO_METADATA_FOR_ATTR_VALUE, DS_REPL_INFO_METADATA_FOR_OBJ, DS_REPL_INFO_NEIGHBORS, DS_REPL_INFO_PENDING_OPS, DsReplicaGetInfo2, DsReplicaGetInfo2 function [Active Directory], DsReplicaGetInfo2W, ad.dsreplicagetinfo2, ntdsapi/DsReplicaGetInfo2, ntdsapi/DsReplicaGetInfo2W
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaGetInfo2W (Unicode)
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
 - DsReplicaGetInfo2W
 - ntdsapi/DsReplicaGetInfo2W
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
 - DsReplicaGetInfo2
 - DsReplicaGetInfo2W
---

# DsReplicaGetInfo2W function


## -description

The <b>DsReplicaGetInfo2</b> function retrieves replication state data from the directory service. This function allows paging of results in cases where there are more than 1000 entries to retrieve.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param InfoType [in]

Contains one of the <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a> values that specifies the type of replication data to retrieve. This value also determines which type of structure is returned in <i>ppInfo</i>.

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



#### DS_REPL_INFO_METADATA_FOR_ATTR_VALUE

<i>pszObject</i> identifies the object for which attribute replication metadata is requested.



#### DS_REPL_INFO_CURSORS_2_FOR_NC



#### DS_REPL_INFO_CURSORS_3_FOR_NC



#### DS_REPL_INFO_METADATA_2_FOR_OBJ

<i>pszObject</i> identifies the object for which replication metadata is requested.



#### DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE

<i>pszObject</i> identifies the object for which attribute replication metadata is requested.

### -param puuidForSourceDsaObjGuid [in, optional]

Pointer to a <b>GUID</b> value that identifies a specific replication source. If this parameter is not <b>NULL</b> and the <i>InfoType</i> parameter contains <b>DS_REPL_INFO_NEIGHBORS</b>, only neighbor data for the source corresponding to the nTDSDSA object with the given <b>objectGuid</b> in the directory is returned. This parameter is ignored if <b>NULL</b> or if the <i>InfoType</i> parameter is anything other than <b>DS_REPL_INFO_NEIGHBORS</b>.

### -param pszAttributeName [in, optional]

Pointer to a null-terminated Unicode string that contains the name of the specific attribute to retrieve replication data for.

This parameter is only used if the <i>InfoType</i> parameter contains one of the following values.

<a id="DS_REPL_INFO_METADATA_FOR_ATTR_VALUE"></a>
<a id="ds_repl_info_metadata_for_attr_value"></a>


#### DS_REPL_INFO_METADATA_FOR_ATTR_VALUE

<a id="DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE"></a>
<a id="ds_repl_info_metadata_2_for_attr_value"></a>


#### DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE

### -param pszValue [in, optional]

Pointer to a null-terminated Unicode string that contains the distinguished name value to match. If the requested attribute is a distinguished name type value, this function return the attributes that contain the specified value.

### -param dwFlags [in]

Contains a set of flags that modify the behavior of the function. This parameter can be zero or the following value.



#### DS_REPL_INFO_FLAG_IMPROVE_LINKED_ATTRS

Causes the attribute metadata to account for metadata on the attribute's linked values.
    The resulting vector represents changes for all attributes. This modified
    vector is useful for clients that expect all attributes and metadata to
    be included in the attribute metadata vector.

### -param dwEnumerationContext [in]

Contains the index of the next entry to retrieve.  This parameter must be set to zero the first time this function is called.

This parameter is only used if the <i>InfoType</i> parameter contains one of the following values.

<a id="DS_REPL_INFO_CURSORS_2_FOR_NC"></a>
<a id="ds_repl_info_cursors_2_for_nc"></a>


#### DS_REPL_INFO_CURSORS_2_FOR_NC

<a id="DS_REPL_INFO_CURSORS_3_FOR_NC"></a>
<a id="ds_repl_info_cursors_3_for_nc"></a>


#### DS_REPL_INFO_CURSORS_3_FOR_NC

<a id="DS_REPL_INFO_METADATA_FOR_ATTR_VALUE"></a>
<a id="ds_repl_info_metadata_for_attr_value"></a>


#### DS_REPL_INFO_METADATA_FOR_ATTR_VALUE

<a id="DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE"></a>
<a id="ds_repl_info_metadata_2_for_attr_value"></a>


#### DS_REPL_INFO_METADATA_2_FOR_ATTR_VALUE

This function will retrieve a maximum of 1000 entries on each call. If after calling this function, more entries are available, the <b>dwEnumerationContext</b> member of the retrieved structure will contain the index of the next entry to retrieve. The <b>dwEnumerationContext</b> member of the retrieved structure is then used as the <i>dwEnumerationContext</i> parameter in the next call to this function. When all of the entries have been retrieved, the <b>dwEnumerationContext</b> member of the retrieved structure will contain -1. If -1 is passed for this parameter, this function will return <b>ERROR_NO_MORE_ITEMS</b>.

### -param ppInfo [out]

Address of a structure pointer that receives the requested data. The value of the <i>InfoType</i> parameter determines the format of this structure. For more information and a list of possible <i>InfoType</i> values and the corresponding structure types, see <a href="/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a>.

The caller must free this memory when it is no longer required by calling <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicafreeinfo">DsReplicaFreeInfo</a>.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error otherwise.
      The following are possible error codes.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicafreeinfo">DsReplicaFreeInfo</a>