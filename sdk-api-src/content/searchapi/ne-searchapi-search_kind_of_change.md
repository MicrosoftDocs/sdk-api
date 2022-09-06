---
UID: NE:searchapi._SEARCH_KIND_OF_CHANGE
title: SEARCH_KIND_OF_CHANGE (searchapi.h)
description: Indicates the kind of change affecting an item when a source sink notifies a client that an item has been changed.
helpviewer_keywords: ["SEARCH_CHANGE_ADD","SEARCH_CHANGE_DELETE","SEARCH_CHANGE_MODIFY","SEARCH_CHANGE_MOVE_RENAME","SEARCH_CHANGE_SEMANTICS_DIRECTORY","SEARCH_CHANGE_SEMANTICS_SHALLOW","SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY","SEARCH_KIND_OF_CHANGE","SEARCH_KIND_OF_CHANGE enumeration [search]","_search_SEARCH_KIND_OF_CHANGE","search._search_SEARCH_KIND_OF_CHANGE","searchapi/SEARCH_CHANGE_ADD","searchapi/SEARCH_CHANGE_DELETE","searchapi/SEARCH_CHANGE_MODIFY","searchapi/SEARCH_CHANGE_MOVE_RENAME","searchapi/SEARCH_CHANGE_SEMANTICS_DIRECTORY","searchapi/SEARCH_CHANGE_SEMANTICS_SHALLOW","searchapi/SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY","searchapi/SEARCH_KIND_OF_CHANGE"]
old-location: search\_search_SEARCH_KIND_OF_CHANGE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_kind_of_change.htm
ms.date: 12/05/2018
ms.keywords: SEARCH_CHANGE_ADD, SEARCH_CHANGE_DELETE, SEARCH_CHANGE_MODIFY, SEARCH_CHANGE_MOVE_RENAME, SEARCH_CHANGE_SEMANTICS_DIRECTORY, SEARCH_CHANGE_SEMANTICS_SHALLOW, SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY, SEARCH_KIND_OF_CHANGE, SEARCH_KIND_OF_CHANGE enumeration [search], _search_SEARCH_KIND_OF_CHANGE, search._search_SEARCH_KIND_OF_CHANGE, searchapi/SEARCH_CHANGE_ADD, searchapi/SEARCH_CHANGE_DELETE, searchapi/SEARCH_CHANGE_MODIFY, searchapi/SEARCH_CHANGE_MOVE_RENAME, searchapi/SEARCH_CHANGE_SEMANTICS_DIRECTORY, searchapi/SEARCH_CHANGE_SEMANTICS_SHALLOW, searchapi/SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY, searchapi/SEARCH_KIND_OF_CHANGE
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: SEARCH_KIND_OF_CHANGE
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _SEARCH_KIND_OF_CHANGE
 - searchapi/_SEARCH_KIND_OF_CHANGE
 - SEARCH_KIND_OF_CHANGE
 - searchapi/SEARCH_KIND_OF_CHANGE
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
 - SEARCH_KIND_OF_CHANGE
---

# SEARCH_KIND_OF_CHANGE enumeration


## -description

Indicates the kind of change affecting an item when a source sink notifies a client that an item has been changed.

## -enum-fields

### -field SEARCH_CHANGE_ADD:0

An item was added.

### -field SEARCH_CHANGE_DELETE:1

An item was deleted.

### -field SEARCH_CHANGE_MODIFY:2

An item was modified.

### -field SEARCH_CHANGE_MOVE_RENAME:3

An item was moved or renamed. Not currently supported for use with <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchpersistentitemschangedsink-onitemschanged">ISearchPersistentItemsChangedSink::OnItemsChanged</a>.

### -field SEARCH_CHANGE_SEMANTICS_DIRECTORY:0x40000

An item is a directory. The item needs to be crawled rather than just reindexed as a document would be.

### -field SEARCH_CHANGE_SEMANTICS_SHALLOW:0x80000

Index directory properties were changed for an item.

### -field SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY:0x400000

Security on an item was changed.

## -remarks

SEARCH_CHANGE_ADD, SEARCH_CHANGE_DELETE, and SEARCH_CHANGE_MODIFY are mutually exclusive. Only one of them can be used at a time. However, any one of them can be combined with the remaining flags.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa965367(v=vs.85)">INLINE_NOTIFY_DATA_CHANGE_ENTRY</a>



<b>Reference</b>



<a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_change">SEARCH_ITEM_CHANGE</a>
