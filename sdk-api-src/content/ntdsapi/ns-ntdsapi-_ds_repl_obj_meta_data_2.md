---
UID: NS:ntdsapi._DS_REPL_OBJ_META_DATA_2
title: "_DS_REPL_OBJ_META_DATA_2"
author: windows-sdk-content
description: The DS_REPL_OBJ_META_DATA_2 structure contains an array of DS_REPL_ATTR_META_DATA_2 structures, which in turn contain replication state data for the attributes (past and present) for a given object, as returned by the DsReplicaGetInfo2 function.
old-location: ad\ds_repl_obj_meta_data_2.htm
old-project: AD
ms.assetid: 2aed753f-432c-4de8-a6be-aa79833f002f
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DS_REPL_OBJ_META_DATA_2, DS_REPL_OBJ_META_DATA_2 structure [Active Directory], _DS_REPL_OBJ_META_DATA_2, ad.ds_repl_obj_meta_data_2, ntdsapi/DS_REPL_OBJ_META_DATA_2
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
tech.root: 
req.typenames: DS_REPL_OBJ_META_DATA_2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdsapi.h
api_name:
-	DS_REPL_OBJ_META_DATA_2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _DS_REPL_OBJ_META_DATA_2 structure


## -description


The <b>DS_REPL_OBJ_META_DATA_2</b> structure contains an array of <a href="https://msdn.microsoft.com/392457b7-df69-44d0-82b2-8381d5877354">DS_REPL_ATTR_META_DATA_2</a> structures, which in turn contain replication state data for the attributes (past and present) for a given object, as returned by the 
<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> function. This structure is an enhanced version of the <a href="https://msdn.microsoft.com/7851ffbc-5d05-4ea7-b3b4-1b8b77299be5">DS_REPL_OBJ_META_DATA</a> structure.


## -struct-fields




### -field cNumEntries

Contains the number of elements in the <b>rgMetaData</b> array.


### -field dwReserved

Not used.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

Contains an array of <a href="https://msdn.microsoft.com/392457b7-df69-44d0-82b2-8381d5877354">DS_REPL_ATTR_META_DATA_2</a> structures. The <b>cNumEntries</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/392457b7-df69-44d0-82b2-8381d5877354">DS_REPL_ATTR_META_DATA_2</a>



<a href="https://msdn.microsoft.com/7851ffbc-5d05-4ea7-b3b4-1b8b77299be5">DS_REPL_OBJ_META_DATA</a>



<a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a>
 

 

