---
UID: NE:searchapi._SEARCH_NOTIFICATION_PRIORITY
title: SEARCH_NOTIFICATION_PRIORITY (searchapi.h)
description: Indicates the priority of processing an item that has changed.
helpviewer_keywords: ["SEARCH_HIGH_PRIORITY","SEARCH_NORMAL_PRIORITY","SEARCH_NOTIFICATION_PRIORITY","SEARCH_NOTIFICATION_PRIORITY enumeration [search]","_search_SEARCH_NOTIFICATION_PRIORITY","search._search_SEARCH_NOTIFICATION_PRIORITY","searchapi/SEARCH_HIGH_PRIORITY","searchapi/SEARCH_NORMAL_PRIORITY","searchapi/SEARCH_NOTIFICATION_PRIORITY"]
old-location: search\_search_SEARCH_NOTIFICATION_PRIORITY.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_notification_priority.htm
ms.date: 12/05/2018
ms.keywords: SEARCH_HIGH_PRIORITY, SEARCH_NORMAL_PRIORITY, SEARCH_NOTIFICATION_PRIORITY, SEARCH_NOTIFICATION_PRIORITY enumeration [search], _search_SEARCH_NOTIFICATION_PRIORITY, search._search_SEARCH_NOTIFICATION_PRIORITY, searchapi/SEARCH_HIGH_PRIORITY, searchapi/SEARCH_NORMAL_PRIORITY, searchapi/SEARCH_NOTIFICATION_PRIORITY
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
req.typenames: SEARCH_NOTIFICATION_PRIORITY
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _SEARCH_NOTIFICATION_PRIORITY
 - searchapi/_SEARCH_NOTIFICATION_PRIORITY
 - SEARCH_NOTIFICATION_PRIORITY
 - searchapi/SEARCH_NOTIFICATION_PRIORITY
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
 - SEARCH_NOTIFICATION_PRIORITY
---

# SEARCH_NOTIFICATION_PRIORITY enumeration


## -description

Indicates the priority of processing an item that has changed.

## -enum-fields

### -field SEARCH_NORMAL_PRIORITY:0

The changed item is added to the end of the indexer's queue.

### -field SEARCH_HIGH_PRIORITY:1

The changed item is placed ahead of other queued items in the indexer's queue, to be processed as soon as possible.

## -remarks

Set the <b>priority</b> member of the <a href="/windows/desktop/api/searchapi/ns-searchapi-search_item_change">SEARCH_ITEM_CHANGE</a> structure to one of these flags.

As the indexer crawls, it builds a list of items that need to be indexed. These flags indicate the placement of changed items in the indexer's queue. Higher priority items are placed at the front of the queue.
