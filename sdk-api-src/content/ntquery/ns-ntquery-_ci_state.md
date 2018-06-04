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

# _CI_STATE structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Represents the current state of an Indexing Service catalog.


## -struct-fields




### -field cbStruct

The size of this structure, in bytes.


### -field cWordList

The number of current word lists.


### -field cPersistentIndex

The number of persistent indexes.


### -field cQueries

The number of actively running queries.


### -field cDocuments

The number of documents waiting to be filtered.


### -field cFreshTest

The number of unique documents in word lists and shadow indexes.


### -field dwMergeProgress

The completion percentage of current merge, if one is running.


### -field eState

The state of content indexing. This can be one or more of the <a href="https://msdn.microsoft.com/c951a3bf-16d3-4f69-8485-c3d62a4fdd17">CI_STATE_*</a> constants. 


### -field cFilteredDocuments

The number of documents filtered since content indexing began.


### -field cTotalDocuments

The total number of documents in the system.


### -field cPendingScans

The number of pending scans, possibly one for each scope in the directories list. The value is usually zero, except immediately after content indexing has been started or after a notification queue overflows.


### -field dwIndexSize

The size, in megabytes, of the index (excluding the property cache).


### -field cUniqueKeys

The number of unique keys in the master index.


### -field cSecQDocuments

The number of documents in the secondary queue, which contains documents that failed filtering due to a sharing violation.


### -field dwPropCacheSize

The size of the property cache, in megabytes.


## -remarks



When using this structure, all members are output values. The <b>cbStruct</b> member is both an input value and an output value.




## -see-also




<a href="https://msdn.microsoft.com/1338815e-11b3-4eb2-9454-212b69d25a2a">CIState</a>



<a href="https://msdn.microsoft.com/c951a3bf-16d3-4f69-8485-c3d62a4fdd17">CI_STATE_* Constants</a>
 

 

