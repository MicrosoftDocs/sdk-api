---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DS_REPL_ATTR_VALUE_META_DATA_EXT structure


## -description


Provides metadata for a collection of attribute replication values.


## -struct-fields




### -field cNumEntries

The number of elements in the <b>rgMetaData</b> array.


### -field dwEnumerationContext

The zero-based index of the next entry to retrieve if more entries are available. This value is passed for 
      the <i>dwEnumerationContext</i> parameter in the next call to 
      <a href="https://msdn.microsoft.com/5735d91d-1b7d-4dc6-b6c6-61ba38ebe50d">DsReplicaGetInfo2</a> to retrieve the next block of 
      entries. If no more entries are available, this member contains -1.


### -field rgMetaData.size_is

 


### -field rgMetaData.size_is.cNumEntries

 


### -field rgMetaData

An array of <a href="https://msdn.microsoft.com/2BE0F9C4-D688-4DE6-8DB2-15666D8BD070">DS_REPL_VALUE_META_DATA_EXT</a> 
      structures that contain the attribute replication  values. The <b>cNumEntries</b> member 
      contains the number of elements in this array.

An array of <a href="https://msdn.microsoft.com/2BE0F9C4-D688-4DE6-8DB2-15666D8BD070">DS_REPL_VALUE_META_DATA_EXT</a> 
      structures that contain the attribute replication values. The <b>cNumEntries</b> member 
      contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/88d8a164-2192-4e73-a190-aa5b5dbb1101">DS_REPL_INFO_TYPE</a>



<a href="https://msdn.microsoft.com/42b20d3b-1799-4f5f-b74e-fe9284dd8ac3">Domain Controller and Replication Management Structures</a>
 

 

