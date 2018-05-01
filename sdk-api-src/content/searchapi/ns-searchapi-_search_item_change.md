---
UID: NS:searchapi._SEARCH_ITEM_CHANGE
title: "_SEARCH_ITEM_CHANGE"
author: windows-driver-content
description: Specifies the changes to an indexed item.
old-location: search\_search_SEARCH_ITEM_CHANGE.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\structures\search_item_change.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SEARCH_ITEM_CHANGE, SEARCH_ITEM_CHANGE structure [search], _SEARCH_ITEM_CHANGE, _search_SEARCH_ITEM_CHANGE, search._search_SEARCH_ITEM_CHANGE, searchapi/SEARCH_ITEM_CHANGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: SEARCH_ITEM_CHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Searchapi.h
api_name:
-	SEARCH_ITEM_CHANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SEARCH_ITEM_CHANGE structure


## -description


Specifies the changes to an indexed item.


## -struct-fields




### -field Change

Type: <b><a href="https://msdn.microsoft.com/b47b18b4-df67-433f-8c10-1a0b444d0f3a">SEARCH_KIND_OF_CHANGE</a></b>

Flag that specifies the kind of change as a value from the 
                <a href="https://msdn.microsoft.com/b47b18b4-df67-433f-8c10-1a0b444d0f3a">SEARCH_KIND_OF_CHANGE</a> enumerated type.


### -field Priority

Type: <b><a href="https://msdn.microsoft.com/b4539914-392f-40b4-8d6b-9069f1fce187">SEARCH_NOTIFICATION_PRIORITY</a></b>

Flag that specifies the priority of processing this change as a value from the <a href="https://msdn.microsoft.com/b4539914-392f-40b4-8d6b-9069f1fce187">SEARCH_NOTIFICATION_PRIORITY</a> enumerated type.


### -field pUserData

Type: <b>BLOB*</b>

Pointer to user information.


### -field lpwszURL

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string containing the URL of the item in a SEARCH_CHANGE_MOVE_RENAME, SEARCH_CHANGE_ADD, or SEARCH_CHANGE_MODIFY notification. In the case of a move, this member contains the new URL of the item.


### -field lpwszOldURL

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string containing the old URL of the item in a SEARCH_CHANGE_MOVE_RENAME or SEARCH_CHANGE_DELETE notification.

