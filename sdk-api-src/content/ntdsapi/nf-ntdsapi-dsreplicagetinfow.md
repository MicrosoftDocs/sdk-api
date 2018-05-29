---
UID: NF:ntdsapi.DsReplicaGetInfoW
title: DsReplicaGetInfoW function
author: windows-sdk-content
description: Retrieves replication state data from the directory service.
old-location: ad\dsreplicagetinfo.htm
old-project: AD
ms.assetid: b7ab22fe-ed92-4213-9b66-2dd5526286fa
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DS_REPL_INFO_CURSORS_FOR_NC, DS_REPL_INFO_KCC_DSA_CONNECT_FAILURES, DS_REPL_INFO_KCC_DSA_LINK_FAILURES, DS_REPL_INFO_METADATA_FOR_OBJ, DS_REPL_INFO_NEIGHBORS, DS_REPL_INFO_PENDING_OPS, DsReplicaGetInfo, DsReplicaGetInfo function [Active Directory], DsReplicaGetInfoW, _glines_dsreplicagetinfo, ad.dsreplicagetinfo, ntdsapi/DsReplicaGetInfo, ntdsapi/DsReplicaGetInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
api_name:
-	DsReplicaGetInfo
-	DsReplicaGetInfoW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# DsReplicaGetInfoW function


## -description


The <b>DsReplicaGetInfo</b> function retrieves replication state data from the directory service.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param InfoType [in]

Contains one of the <a href="https://msdn.microsoft.com/88d8a164-2192-4e73-a190-aa5b5dbb1101">DS_REPL_INFO_TYPE</a> values that specifies the type of replication data to retrieve. This value also determines which type of structure is returned in <i>ppInfo</i>.

Only the following values are supported for this function. If other data types are required, the <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function must be used.

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

Address of a structure pointer that receives the requested data. The value of the <i>InfoType</i> parameter determines the format of this structure. For more information and list of possible <i>InfoType</i> values and the corresponding structure types, see <a href="https://msdn.microsoft.com/88d8a164-2192-4e73-a190-aa5b5dbb1101">DS_REPL_INFO_TYPE</a>.

The caller must free this memory when it is no longer required by calling <a href="https://msdn.microsoft.com/32ce378e-a178-4970-b3bd-3887866e97af">DsReplicaFreeInfo</a>.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error otherwise.
      The following are possible error codes.




## -see-also




<a href="https://msdn.microsoft.com/88d8a164-2192-4e73-a190-aa5b5dbb1101">DS_REPL_INFO_TYPE</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/32ce378e-a178-4970-b3bd-3887866e97af">DsReplicaFreeInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

