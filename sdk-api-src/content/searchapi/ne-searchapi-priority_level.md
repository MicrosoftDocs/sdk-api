---
UID: NE:searchapi.__MIDL___MIDL_itf_searchapi_0000_0022_0001
title: PRIORITY_LEVEL (searchapi.h)
description: Used by the IRowsetPrioritization interface to sets or retrieve the current indexer prioritization level for the scope specified by a query.
helpviewer_keywords: ["PRIORITY_LEVEL","PRIORITY_LEVEL enumeration [search]","PRIORITY_LEVEL_DEFAULT","PRIORITY_LEVEL_FOREGROUND","PRIORITY_LEVEL_HIGH","PRIORITY_LEVEL_LOW","_search_PRIORITY_LEVEL","search._search_PRIORITY_LEVEL","searchapi/PRIORITY_LEVEL","searchapi/PRIORITY_LEVEL_DEFAULT","searchapi/PRIORITY_LEVEL_FOREGROUND","searchapi/PRIORITY_LEVEL_HIGH","searchapi/PRIORITY_LEVEL_LOW"]
old-location: search\_search_PRIORITY_LEVEL.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\priority_level.htm
ms.date: 12/05/2018
ms.keywords: PRIORITY_LEVEL, PRIORITY_LEVEL enumeration [search], PRIORITY_LEVEL_DEFAULT, PRIORITY_LEVEL_FOREGROUND, PRIORITY_LEVEL_HIGH, PRIORITY_LEVEL_LOW, _search_PRIORITY_LEVEL, search._search_PRIORITY_LEVEL, searchapi/PRIORITY_LEVEL, searchapi/PRIORITY_LEVEL_DEFAULT, searchapi/PRIORITY_LEVEL_FOREGROUND, searchapi/PRIORITY_LEVEL_HIGH, searchapi/PRIORITY_LEVEL_LOW
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PRIORITY_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_searchapi_0000_0022_0001
 - searchapi/__MIDL___MIDL_itf_searchapi_0000_0022_0001
 - PRIORITY_LEVEL
 - searchapi/PRIORITY_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - PRIORITY_LEVEL
---

# PRIORITY_LEVEL enumeration


## -description

Used by the <a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a> interface to set or retrieve the current indexer prioritization level for the scope specified by a query.

## -enum-fields

### -field PRIORITY_LEVEL_FOREGROUND:0

Indicates that the indexer should process items as fast as the machine allows.

### -field PRIORITY_LEVEL_HIGH:1

Indicates that the indexer should process items in this scope first, and as quickly as possible.

### -field PRIORITY_LEVEL_LOW:2

Indicates that the indexer should process items in this scope before those at the normal rate, but after any other prioritization requests.

### -field PRIORITY_LEVEL_DEFAULT:3

Indicates that the indexer should  process items at the normal indexer rate.

## -remarks

Check out the <a href="/windows/win32/search/-search-sample-searchevents">SearchEvents code sample</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/searchapi/nn-searchapi-irowsetprioritization">IRowsetPrioritization</a>



<a href="/windows/desktop/search/indexing-prioritization-and-rowset-events">Indexing Prioritization and Rowset Events in Windows 7</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags">PRIORITIZE_FLAGS</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate">ROWSETEVENT_ITEMSTATE</a>



<a href="/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type">ROWSETEVENT_TYPE</a>



<b>Reference</b>



<a href="/windows/desktop/search/-search-sql-rowset-properties">Rowset Properties</a>
