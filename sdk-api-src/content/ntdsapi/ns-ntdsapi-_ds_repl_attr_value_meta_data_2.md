---
UID: NS:ntdsapi._DS_REPL_ATTR_VALUE_META_DATA_2
title: "_DS_REPL_ATTR_VALUE_META_DATA_2"
author: windows-sdk-content
description: Used with the DsReplicaGetInfo2 function to provide metadata for a collection of attribute values.
old-location: ad\ds_repl_attr_value_meta_data_2.htm
tech.root: ad
ms.assetid: 2022362a-e2f7-4cfd-a512-cfe29e5d439d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DS_REPL_ATTR_VALUE_META_DATA_2, DS_REPL_ATTR_VALUE_META_DATA_2 structure [Active Directory], _DS_REPL_ATTR_VALUE_META_DATA_2, ad.ds_repl_attr_value_meta_data_2, ntdsapi/DS_REPL_ATTR_VALUE_META_DATA_2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - DS_REPL_ATTR_VALUE_META_DATA_2
product: Windows
targetos: Windows
req.typenames: DS_REPL_ATTR_VALUE_META_DATA_2
req.redist: 
---

# _DS_REPL_ATTR_VALUE_META_DATA_2 structure


## -description


The <b>DS_REPL_ATTR_VALUE_META_DATA_2</b> structure is used with the <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function to provide metadata for a collection of attribute values.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwEnumerationContext

Contains the zero-based index of the next entry to retrieve if more entries are available. This value is passed for the <i>dwEnumerationContext</i> parameter in the next call to <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> to retrieve the next block of entries. If no more entries are available, this member contains -1.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

Contains an array of <a href="https://msdn.microsoft.com/747e32b8-2cc0-4fcd-88dc-027188598361">DS_REPL_VALUE_META_DATA_2</a> structures that contain the individual attribute replication values. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/747e32b8-2cc0-4fcd-88dc-027188598361">DS_REPL_VALUE_META_DATA_2</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

