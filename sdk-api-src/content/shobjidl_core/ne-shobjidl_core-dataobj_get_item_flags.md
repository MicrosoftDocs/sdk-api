---
UID: NE:shobjidl_core.DATAOBJ_GET_ITEM_FLAGS
title: DATAOBJ_GET_ITEM_FLAGS
author: windows-sdk-content
description: Values used by the SHGetItemFromDataObject function to specify options concerning the processing of the source object.
old-location: shell\DATAOBJ_GET_ITEM_FLAGS.htm
tech.root: shell
ms.assetid: 7a5ee490-cf30-452a-ade2-22d875ce0358
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DATAOBJ_GET_ITEM_FLAGS, DATAOBJ_GET_ITEM_FLAGS enumeration [Windows Shell], DOGIF_DEFAULT, DOGIF_NO_HDROP, DOGIF_NO_URL, DOGIF_ONLY_IF_ONE, DOGIF_TRAVERSE_LINK, _shell_DATAOBJ_GET_ITEM_FLAGS, shell.DATAOBJ_GET_ITEM_FLAGS, shobjidl_core/DATAOBJ_GET_ITEM_FLAGS, shobjidl_core/DOGIF_DEFAULT, shobjidl_core/DOGIF_NO_HDROP, shobjidl_core/DOGIF_NO_URL, shobjidl_core/DOGIF_ONLY_IF_ONE, shobjidl_core/DOGIF_TRAVERSE_LINK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - DATAOBJ_GET_ITEM_FLAGS
product: Windows
targetos: Windows
req.typenames: DATAOBJ_GET_ITEM_FLAGS
req.redist: 
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

