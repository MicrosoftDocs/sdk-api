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
 

 

