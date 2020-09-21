---
UID: NS:ntdsapi._DS_REPL_OBJ_META_DATA
title: DS_REPL_OBJ_META_DATA (ntdsapi.h)
description: The DS_REPL_OBJ_META_DATA structure contains an array of DS_REPL_ATTR_META_DATA structures. These structures contain replication state data for past and present attributes for a given object.
helpviewer_keywords: ["DS_REPL_OBJ_META_DATA","DS_REPL_OBJ_META_DATA structure [Active Directory]","_glines_ds_repl_obj_meta_data","ad.ds__repl__obj__meta__data","ad.ds_repl_obj_meta_data","ntdsapi/DS_REPL_OBJ_META_DATA"]
old-location: ad\ds_repl_obj_meta_data.htm
tech.root: ad
ms.assetid: 7851ffbc-5d05-4ea7-b3b4-1b8b77299be5
ms.date: 12/05/2018
ms.keywords: DS_REPL_OBJ_META_DATA, DS_REPL_OBJ_META_DATA structure [Active Directory], _glines_ds_repl_obj_meta_data, ad.ds__repl__obj__meta__data, ad.ds_repl_obj_meta_data, ntdsapi/DS_REPL_OBJ_META_DATA
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
req.typenames: DS_REPL_OBJ_META_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_OBJ_META_DATA
 - ntdsapi/_DS_REPL_OBJ_META_DATA
 - DS_REPL_OBJ_META_DATA
 - ntdsapi/DS_REPL_OBJ_META_DATA
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
 - DS_REPL_OBJ_META_DATA
---

# DS_REPL_OBJ_META_DATA structure


## -description

The <b>DS_REPL_OBJ_META_DATA</b> structure contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data">DS_REPL_ATTR_META_DATA</a> structures. These structures contain replication state data for past and present attributes for a given object. The replication state data is returned from the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a> and <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> functions. The metadata records data about the last modification of a given object attribute.

## -struct-fields

### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.

### -field dwReserved

Not used.

### -field rgMetaData.size_is

### -field rgMetaData.size_is.cNumEntries

### -field rgMetaData

Contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data">DS_REPL_ATTR_META_DATA</a> structures. The <b>cNumEntries</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data">DS_REPL_ATTR_META_DATA</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfow">DsReplicaGetInfo</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>