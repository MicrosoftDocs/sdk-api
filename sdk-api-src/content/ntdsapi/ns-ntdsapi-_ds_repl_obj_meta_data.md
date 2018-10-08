---
UID: NS:ntdsapi._DS_REPL_OBJ_META_DATA
title: "_DS_REPL_OBJ_META_DATA"
author: windows-sdk-content
description: The DS_REPL_OBJ_META_DATA structure contains an array of DS_REPL_ATTR_META_DATA structures. These structures contain replication state data for past and present attributes for a given object.
old-location: ad\ds_repl_obj_meta_data.htm
tech.root: ad
ms.assetid: 7851ffbc-5d05-4ea7-b3b4-1b8b77299be5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DS_REPL_OBJ_META_DATA, DS_REPL_OBJ_META_DATA structure [Active Directory], _DS_REPL_OBJ_META_DATA, _glines_ds_repl_obj_meta_data, ad.ds__repl__obj__meta__data, ad.ds_repl_obj_meta_data, ntdsapi/DS_REPL_OBJ_META_DATA
ms.prod: windows
ms.technology: windows-sdk
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
 - DS_REPL_OBJ_META_DATA
product: Windows
targetos: Windows
req.typenames: DS_REPL_OBJ_META_DATA
req.redist: 
---

# _DS_REPL_OBJ_META_DATA structure


## -description


The <b>DS_REPL_OBJ_META_DATA</b> structure contains an array of <a href="https://msdn.microsoft.com/27ccc1c9-03d7-4d13-b9ec-65d6b8bdfd37">DS_REPL_ATTR_META_DATA</a> structures. These structures contain replication state data for past and present attributes for a given object. The replication state data is returned from the 
<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a> and <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> functions. The metadata records data about the last modification of a given object attribute.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwReserved

Not used.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

Contains an array of <a href="https://msdn.microsoft.com/27ccc1c9-03d7-4d13-b9ec-65d6b8bdfd37">DS_REPL_ATTR_META_DATA</a> structures. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/27ccc1c9-03d7-4d13-b9ec-65d6b8bdfd37">DS_REPL_ATTR_META_DATA</a>



<a href="https://msdn.microsoft.com/b7ab22fe-ed92-4213-9b66-2dd5526286fa">DsReplicaGetInfo</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

