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

