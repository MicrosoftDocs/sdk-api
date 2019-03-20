---
UID: NS:ntdsapi._DS_REPL_ATTR_VALUE_META_DATA
title: DS_REPL_ATTR_VALUE_META_DATA (ntdsapi.h)
author: windows-sdk-content
description: The DS_REPL_ATTR_VALUE_META_DATA structure is used with the DsReplicaGetInfo2 function to provide metadata for a collection of attribute values.
old-location: ad\ds_repl_attr_value_meta_data.htm
tech.root: ad
ms.assetid: b13cdd31-d154-4539-81d6-d7a449e2b3d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DS_REPL_ATTR_VALUE_META_DATA, DS_REPL_ATTR_VALUE_META_DATA structure [Active Directory], ad.ds_repl_attr_value_meta_data, ntdsapi/DS_REPL_ATTR_VALUE_META_DATA
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
 - DS_REPL_ATTR_VALUE_META_DATA
product: Windows
targetos: Windows
req.typenames: DS_REPL_ATTR_VALUE_META_DATA
req.redist: 
---

# DS_REPL_ATTR_VALUE_META_DATA structure


## -description


The <b>DS_REPL_ATTR_VALUE_META_DATA</b> structure is used with the <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function to provide metadata for a collection of attribute values.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwEnumerationContext

Contains the zero-based index of the next entry to retrieve if more entries are available. This value is passed for the <i>dwEnumerationContext</i> parameter in the next call to <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> to retrieve the next block of entries. If no more entries are available, this member contains -1.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

Contains an array of <a href="https://msdn.microsoft.com/294a466e-8a83-4b33-a8a8-ac7b51d081d4">DS_REPL_VALUE_META_DATA</a> structures that contain the individual attribute replication values. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/294a466e-8a83-4b33-a8a8-ac7b51d081d4">DS_REPL_VALUE_META_DATA</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

