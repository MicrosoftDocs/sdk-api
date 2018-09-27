---
UID: NE:searchapi._SEARCH_KIND_OF_CHANGE
title: "_SEARCH_KIND_OF_CHANGE"
author: windows-sdk-content
description: Indicates the kind of change affecting an item when a source sink notifies a client that an item has been changed.
old-location: search\_search_SEARCH_KIND_OF_CHANGE.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_kind_of_change.htm
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SEARCH_CHANGE_ADD, SEARCH_CHANGE_DELETE, SEARCH_CHANGE_MODIFY, SEARCH_CHANGE_MOVE_RENAME, SEARCH_CHANGE_SEMANTICS_DIRECTORY, SEARCH_CHANGE_SEMANTICS_SHALLOW, SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY, SEARCH_KIND_OF_CHANGE, SEARCH_KIND_OF_CHANGE enumeration [search], _SEARCH_KIND_OF_CHANGE, _search_SEARCH_KIND_OF_CHANGE, search._search_SEARCH_KIND_OF_CHANGE, searchapi/SEARCH_CHANGE_ADD, searchapi/SEARCH_CHANGE_DELETE, searchapi/SEARCH_CHANGE_MODIFY, searchapi/SEARCH_CHANGE_MOVE_RENAME, searchapi/SEARCH_CHANGE_SEMANTICS_DIRECTORY, searchapi/SEARCH_CHANGE_SEMANTICS_SHALLOW, searchapi/SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY, searchapi/SEARCH_KIND_OF_CHANGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - SEARCH_KIND_OF_CHANGE
product: Windows
targetos: Windows
req.typenames: SEARCH_KIND_OF_CHANGE
req.redist: Windows Desktop Search (WDS) 3.0
---

# _SEARCH_KIND_OF_CHANGE enumeration


## -description


Indicates the kind of change affecting an item when a source sink notifies a client that an item has been changed.
        


## -enum-fields




### -field SEARCH_CHANGE_ADD

An item was added.


### -field SEARCH_CHANGE_DELETE

An item was deleted.


### -field SEARCH_CHANGE_MODIFY

An item was modified.


### -field SEARCH_CHANGE_MOVE_RENAME

An item was moved or renamed. Not currently supported for use with <a href="https://msdn.microsoft.com/975f687f-65c7-4086-b99c-c1b1419a701b">ISearchPersistentItemsChangedSink::OnItemsChanged</a>. 


### -field SEARCH_CHANGE_SEMANTICS_DIRECTORY

An item is a directory. The item needs to be crawled rather than just reindexed as a document would be.


### -field SEARCH_CHANGE_SEMANTICS_SHALLOW

Index directory properties were changed for an item.


### -field SEARCH_CHANGE_SEMANTICS_UPDATE_SECURITY

Security on an item was changed.


## -remarks



SEARCH_CHANGE_ADD, SEARCH_CHANGE_DELETE, and SEARCH_CHANGE_MODIFY are mutually exclusive. Only one of them can be used at a time. However, any one of them can be combined with the remaining flags.




## -see-also




<a href="https://msdn.microsoft.com/95ab0424-e21a-4a5f-b1ce-f40423790125">INLINE_NOTIFY_DATA_CHANGE_ENTRY</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/83ed1c76-7210-4d0b-a6e2-461bc331e168">SEARCH_ITEM_CHANGE</a>
 

 

