---
UID: NS:searchapi._SEARCH_ITEM_CHANGE
title: SEARCH_ITEM_CHANGE (searchapi.h)
description: Specifies the changes to an indexed item.
helpviewer_keywords: ["SEARCH_ITEM_CHANGE","SEARCH_ITEM_CHANGE structure [search]","_search_SEARCH_ITEM_CHANGE","search._search_SEARCH_ITEM_CHANGE","searchapi/SEARCH_ITEM_CHANGE"]
old-location: search\_search_SEARCH_ITEM_CHANGE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\search_item_change.htm
ms.date: 12/05/2018
ms.keywords: SEARCH_ITEM_CHANGE, SEARCH_ITEM_CHANGE structure [search], _search_SEARCH_ITEM_CHANGE, search._search_SEARCH_ITEM_CHANGE, searchapi/SEARCH_ITEM_CHANGE
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
req.typenames: SEARCH_ITEM_CHANGE
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _SEARCH_ITEM_CHANGE
 - searchapi/_SEARCH_ITEM_CHANGE
 - SEARCH_ITEM_CHANGE
 - searchapi/SEARCH_ITEM_CHANGE
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
 - SEARCH_ITEM_CHANGE
---

# SEARCH_ITEM_CHANGE structure


## -description

Specifies the changes to an indexed item.

## -struct-fields

### -field Change

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_kind_of_change">SEARCH_KIND_OF_CHANGE</a></b>

Flag that specifies the kind of change as a value from the 
                <a href="/windows/desktop/api/searchapi/ne-searchapi-search_kind_of_change">SEARCH_KIND_OF_CHANGE</a> enumerated type.

### -field Priority

Type: <b><a href="/windows/desktop/api/searchapi/ne-searchapi-search_notification_priority">SEARCH_NOTIFICATION_PRIORITY</a></b>

Flag that specifies the priority of processing this change as a value from the <a href="/windows/desktop/api/searchapi/ne-searchapi-search_notification_priority">SEARCH_NOTIFICATION_PRIORITY</a> enumerated type.

### -field pUserData

Type: <b>BLOB*</b>

Pointer to user information.

### -field lpwszURL

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string containing the URL of the item in a SEARCH_CHANGE_MOVE_RENAME, SEARCH_CHANGE_ADD, or SEARCH_CHANGE_MODIFY notification. In the case of a move, this member contains the new URL of the item.

### -field lpwszOldURL

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string containing the old URL of the item in a SEARCH_CHANGE_MOVE_RENAME or SEARCH_CHANGE_DELETE notification.