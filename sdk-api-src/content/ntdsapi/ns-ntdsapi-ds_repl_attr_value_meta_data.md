---
UID: NS:ntdsapi._DS_REPL_ATTR_VALUE_META_DATA
title: DS_REPL_ATTR_VALUE_META_DATA (ntdsapi.h)
description: The DS_REPL_ATTR_VALUE_META_DATA structure is used with the DsReplicaGetInfo2 function to provide metadata for a collection of attribute values.
helpviewer_keywords: ["DS_REPL_ATTR_VALUE_META_DATA","DS_REPL_ATTR_VALUE_META_DATA structure [Active Directory]","ad.ds_repl_attr_value_meta_data","ntdsapi/DS_REPL_ATTR_VALUE_META_DATA"]
old-location: ad\ds_repl_attr_value_meta_data.htm
tech.root: ad
ms.assetid: b13cdd31-d154-4539-81d6-d7a449e2b3d5
ms.date: 12/05/2018
ms.keywords: DS_REPL_ATTR_VALUE_META_DATA, DS_REPL_ATTR_VALUE_META_DATA structure [Active Directory], ad.ds_repl_attr_value_meta_data, ntdsapi/DS_REPL_ATTR_VALUE_META_DATA
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
req.typenames: DS_REPL_ATTR_VALUE_META_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_ATTR_VALUE_META_DATA
 - ntdsapi/_DS_REPL_ATTR_VALUE_META_DATA
 - DS_REPL_ATTR_VALUE_META_DATA
 - ntdsapi/DS_REPL_ATTR_VALUE_META_DATA
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
 - DS_REPL_ATTR_VALUE_META_DATA
---

# DS_REPL_ATTR_VALUE_META_DATA structure


## -description

The <b>DS_REPL_ATTR_VALUE_META_DATA</b> structure is used with the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> function to provide metadata for a collection of attribute values.

## -struct-fields

### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.

### -field dwEnumerationContext

Contains the zero-based index of the next entry to retrieve if more entries are available. This value is passed for the <i>dwEnumerationContext</i> parameter in the next call to <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> to retrieve the next block of entries. If no more entries are available, this member contains -1.

### -field rgMetaData.size_is

### -field rgMetaData.size_is.cNumEntries

### -field rgMetaData

Contains an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_value_meta_data">DS_REPL_VALUE_META_DATA</a> structures that contain the individual attribute replication values. The <b>cNumEntries</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_value_meta_data">DS_REPL_VALUE_META_DATA</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a>