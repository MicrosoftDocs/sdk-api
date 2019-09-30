---
UID: NE:searchapi.tagPRIORITIZE_FLAGS
title: tagPRIORITIZE_FLAGS (searchapi.h)
author: windows-sdk-content
description: Used by PrioritizeMatchingURLs to specify how to process items the indexer has previously failed to index.
old-location: search\_search_PRIORITIZE_FLAGS.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\prioritize_flags.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PRIORITIZE_FLAGS, PRIORITIZE_FLAGS enumeration [search], PRIORITIZE_FLAG_IGNOREFAILURECOUNT, PRIORITIZE_FLAG_RETRYFAILEDITEMS, _search_PRIORITIZE_FLAGS, search._search_PRIORITIZE_FLAGS, searchapi/PRIORITIZE_FLAGS, searchapi/PRIORITIZE_FLAG_IGNOREFAILURECOUNT, searchapi/PRIORITIZE_FLAG_RETRYFAILEDITEMS, tagPRIORITIZE_FLAGS
ms.topic: enum
f1_keywords: 
 - "searchapi/PRIORITIZE_FLAGS"
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
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
 - Searchapi.h
api_name:
 - PRIORITIZE_FLAGS
targetos: Windows
req.typenames: 
req.redist: Windows Search (WS) 4.0
ms.custom: 19H1
---

# tagPRIORITIZE_FLAGS enumeration


## -description


Used by <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager2-prioritizematchingurls">PrioritizeMatchingURLs</a> to specify how to process items the indexer has previously failed to index.


## -enum-fields




### -field PRIORITIZE_FLAG_RETRYFAILEDITEMS

Indicates that the indexer should reattempt to index items that it failed to index previously.


### -field PRIORITIZE_FLAG_IGNOREFAILURECOUNT

Indicates that the indexer should continue to reattempt indexing items regardless of the number of times the indexer has failed to index them previously.


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="https://docs.microsoft.com/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-priority_level">PRIORITY_LEVEL</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="https://docs.microsoft.com/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
 

 

