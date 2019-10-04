---
UID: NS:ntdsapi._DS_REPL_ATTR_VALUE_META_DATA_EXT
title: DS_REPL_ATTR_VALUE_META_DATA_EXT (ntdsapi.h)
author: windows-sdk-content
description: Provides metadata for a collection of attribute replication values.
old-location: ad\ds_repl_attr_value_meta_data_ext.htm
tech.root: ad
ms.assetid: CA41C6BF-A485-4AC7-B761-3A07159C2FF1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DS_REPL_ATTR_VALUE_META_DATA_EXT, DS_REPL_ATTR_VALUE_META_DATA_EXT structure [Active Directory], ad.ds_repl_attr_value_meta_data_ext, ntdsapi/DS_REPL_ATTR_VALUE_META_DATA_EXT
ms.topic: struct
f1_keywords:
- ntdsapi/DS_REPL_ATTR_VALUE_META_DATA_EXT
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
- DS_REPL_ATTR_VALUE_META_DATA_EXT
targetos: Windows
req.typenames: DS_REPL_ATTR_VALUE_META_DATA_EXT
req.redist: 
ms.custom: 19H1
---

# DS_REPL_ATTR_VALUE_META_DATA_EXT structure


## -description


Provides metadata for a collection of attribute replication values.


## -struct-fields




### -field cNumEntries

The number of elements in the <b>rgMetaData</b> array.


### -field dwEnumerationContext

The zero-based index of the next entry to retrieve if more entries are available. This value is passed for 
      the <i>dwEnumerationContext</i> parameter in the next call to 
      <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicagetinfo2w">DsReplicaGetInfo2</a> to retrieve the next block of 
      entries. If no more entries are available, this member contains -1.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

An array of <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext">DS_REPL_VALUE_META_DATA_EXT</a> 
      structures that contain the attribute replication  values. The <b>cNumEntries</b> member 
      contains the number of elements in this array.

An array of <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext">DS_REPL_VALUE_META_DATA_EXT</a> 
      structures that contain the attribute replication values. The <b>cNumEntries</b> member 
      contains the number of elements in this array.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repl_info_type">DS_REPL_INFO_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>
 

 

