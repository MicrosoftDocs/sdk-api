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

# _SEARCH_ITEM_PERSISTENT_CHANGE structure


## -description


Contains information about the kind of change that has occurred in an item to be indexed.  This structure is used with the <a href="https://msdn.microsoft.com/975f687f-65c7-4086-b99c-c1b1419a701b">ISearchPersistentItemsChangedSink::OnItemsChanged</a> method to pass information to the indexer about what has changed.


## -struct-fields




### -field Change

Type: <b><a href="https://msdn.microsoft.com/b47b18b4-df67-433f-8c10-1a0b444d0f3a">SEARCH_KIND_OF_CHANGE</a></b>

A value from the <a href="https://msdn.microsoft.com/b47b18b4-df67-433f-8c10-1a0b444d0f3a">SEARCH_KIND_OF_CHANGE</a> enumerated type that indicates the kind of change.


### -field URL

Type: <b>LPWSTR</b>

Pointer to a null-terminated Unicode string containing the URL of the item in a SEARCH_CHANGE_ADD, SEARCH_CHANGE_MODIFY, or SEARCH_CHANGE_DELETE notification. In the case of a move, this member contains the new URL of the item.


### -field OldURL

 


### -field Priority

Type: <b><a href="https://msdn.microsoft.com/b4539914-392f-40b4-8d6b-9069f1fce187">SEARCH_NOTIFICATION_PRIORITY</a></b>

A value from the <a href="https://msdn.microsoft.com/b4539914-392f-40b4-8d6b-9069f1fce187">SEARCH_NOTIFICATION_PRIORITY</a> enumerated type that indicates the priority of the change.


## -remarks



SEARCH_CHANGE_MOVE_RENAME is not supported for use with <a href="https://msdn.microsoft.com/975f687f-65c7-4086-b99c-c1b1419a701b">ISearchPersistentItemsChangedSink::OnItemsChanged</a>.
            



