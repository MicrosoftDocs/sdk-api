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

# GetMenuPosFromID function


## -description


<p class="CCE_Message">[<b>GetMenuPosFromID</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines the position of an item in a menu. Used in the case where the item's ID is known.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

The handle of the menu.


### -param id

Type: <b>UINT</b>

An application-defined 16-bit value that identifies the menu item.


## -returns



Type: <b>int</b>

The item's zero-based position in the menu.




## -remarks



Beginning with Windows Vista, this function is declared in Shlwapi.h.

<b>Windows XP:  </b>This function is declared in Shlwapi.dll.



