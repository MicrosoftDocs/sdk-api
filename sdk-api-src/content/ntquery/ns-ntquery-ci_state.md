---
UID: NS:ntquery._CI_STATE
title: CI_STATE (ntquery.h)
description: Represents the current state of an Indexing Service catalog.helpviewer_keywords: ["CI_STATE","CI_STATE structure [Indexing Service]","_idxs_CI_STATE","indexsrv.ci_state","ntquery/CI_STATE"]
old-location: indexsrv\ci_state.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_2qjp.htm
ms.date: 12/05/2018
ms.keywords: CI_STATE, CI_STATE structure [Indexing Service], _idxs_CI_STATE, indexsrv.ci_state, ntquery/CI_STATE
f1_keywords:
- ntquery/CI_STATE
dev_langs:
- c++
req.header: ntquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- Ntquery.h
api_name:
- CI_STATE
targetos: Windows
req.typenames: CI_STATE
req.redist: 
ms.custom: 19H1
---

# CI_STATE structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="https://www.microsoft.com/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

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

The state of content indexing. This can be one or more of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/ci-state-constants">CI_STATE_*</a> constants. 


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




[CIState](/windows/win32/api/ntquery/ns-ntquery-ci_state)a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/ci-state-constants">CI_STATE_* Constants</a>
 

 

