---
UID: NS:searchapi._SEARCH_ITEM_PERSISTENT_CHANGE
title: SEARCH_ITEM_PERSISTENT_CHANGE (searchapi.h)
description: Contains information about the kind of change that has occurred in an item to be indexed. This structure is used with the ISearchPersistentItemsChangedSink::OnItemsChanged method to pass information to the indexer about what has changed.
helpviewer_keywords: ["SEARCH_ITEM_PERSISTENT_CHANGE","SEARCH_ITEM_PERSISTENT_CHANGE structure [search]","_search_SEARCH_ITEM_PERSISTENT_CHANGE","search._search_SEARCH_ITEM_PERSISTENT_CHANGE","searchapi/SEARCH_ITEM_PERSISTENT_CHANGE"]
old-location: search\_search_SEARCH_ITEM_PERSISTENT_CHANGE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\search_item_persistent_change.htm
ms.date: 12/05/2018
ms.keywords: SEARCH_ITEM_PERSISTENT_CHANGE, SEARCH_ITEM_PERSISTENT_CHANGE structure [search], _search_SEARCH_ITEM_PERSISTENT_CHANGE, search._search_SEARCH_ITEM_PERSISTENT_CHANGE, searchapi/SEARCH_ITEM_PERSISTENT_CHANGE
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchnotifications.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SEARCH_ITEM_PERSISTENT_CHANGE
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _SEARCH_ITEM_PERSISTENT_CHANGE
 - searchapi/_SEARCH_ITEM_PERSISTENT_CHANGE
 - SEARCH_ITEM_PERSISTENT_CHANGE
 - searchapi/SEARCH_ITEM_PERSISTENT_CHANGE
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
 - SEARCH_ITEM_PERSISTENT_CHANGE
---

# SEARCH_ITEM_PERSISTENT_CHANGE structure


## -description

Contains information about the kind of change that has occurred in an item to be indexed.  This structure is used with the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchpersistentitemschangedsink-onitemschanged">ISearchPersistentItemsChangedSink::OnItemsChanged</a> method to pass information to the indexer about what has changed.

## -struct-fields

### -field Change

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_kind_of_change">SEARCH_KIND_OF_CHANGE</a></b>

A value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_kind_of_change">SEARCH_KIND_OF_CHANGE</a> enumerated type that indicates the kind of change.

### -field URL

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string containing the URL of the item in a SEARCH_CHANGE_ADD, SEARCH_CHANGE_MODIFY, or SEARCH_CHANGE_DELETE notification. In the case of a move, this member contains the new URL of the item.

### -field OldURL

### -field Priority

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_notification_priority">SEARCH_NOTIFICATION_PRIORITY</a></b>

A value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_notification_priority">SEARCH_NOTIFICATION_PRIORITY</a> enumerated type that indicates the priority of the change.

## -remarks

SEARCH_CHANGE_MOVE_RENAME is not supported for use with <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchpersistentitemschangedsink-onitemschanged">ISearchPersistentItemsChangedSink::OnItemsChanged</a>.