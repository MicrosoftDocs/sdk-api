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

# DATAOBJ_GET_ITEM_FLAGS enumeration


## -description


Values used by the <a href="https://msdn.microsoft.com/1d7b9ffa-9980-4d68-85e4-7bab667be168">SHGetItemFromDataObject</a> function to specify options concerning the processing of the source object.


## -enum-fields




### -field DOGIF_DEFAULT

0x0000. No special options.


### -field DOGIF_TRAVERSE_LINK

0x0001. If the source object is a link, base the <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> on the link's target rather than the link file itself.


### -field DOGIF_NO_HDROP

0x0002. If the source data object does not contain data in the CFSTR_SHELLIDLIST format, which identifies the object through an IDList, do not revert to the <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CF_HDROP</a> format, which uses a file path, as an alternative in the transfer.


### -field DOGIF_NO_URL

0x0004. If the source data object does not contain data in the CFSTR_SHELLIDLIST format, which identifies the object through an IDList, do not revert to the <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CFSTR_INETURL</a> clipboard format, which uses a URL, as an alternative in the transfer.


### -field DOGIF_ONLY_IF_ONE

0x0008. If the source object is an array of items, use it only if the array contains just one item.

