---
UID: NS:ntdsapi._DS_REPL_OBJ_META_DATA_2
title: DS_REPL_OBJ_META_DATA_2 (ntdsapi.h)
description: The DS_REPL_OBJ_META_DATA_2 structure contains an array of DS_REPL_ATTR_META_DATA_2 structures, which in turn contain replication state data for the attributes (past and present) for a given object, as returned by the DsReplicaGetInfo2 function.
helpviewer_keywords: ["DS_REPL_OBJ_META_DATA_2","DS_REPL_OBJ_META_DATA_2 structure [Active Directory]","ad.ds_repl_obj_meta_data_2","ntdsapi/DS_REPL_OBJ_META_DATA_2"]
old-location: ad\ds_repl_obj_meta_data_2.htm
tech.root: ad
ms.assetid: 2aed753f-432c-4de8-a6be-aa79833f002f
ms.date: 12/05/2018
ms.keywords: DS_REPL_OBJ_META_DATA_2, DS_REPL_OBJ_META_DATA_2 structure [Active Directory], ad.ds_repl_obj_meta_data_2, ntdsapi/DS_REPL_OBJ_META_DATA_2
f1_keywords:
- ntdsapi/DS_REPL_OBJ_META_DATA_2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Ntdsapi.h
api_name:
- DS_REPL_OBJ_META_DATA_2
targetos: Windows
req.typenames: DS_REPL_OBJ_META_DATA_2
req.redist: 
ms.custom: 19H1
---

# DS_REPL_OBJ_META_DATA_2 structure


## -description


The <b>DS_REPL_OBJ_META_DATA_2</b> structure contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2">DS_REPL_ATTR_META_DATA_2</a> structures, which in turn contain replication state data for the attributes (past and present) for a given object, as returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function. This structure is an enhanced version of the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data">DS_REPL_OBJ_META_DATA</a> structure.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwReserved

Not used.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

Contains an array of <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2">DS_REPL_ATTR_META_DATA_2</a> structures. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2">DS_REPL_ATTR_META_DATA_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data">DS_REPL_OBJ_META_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>
 

 

