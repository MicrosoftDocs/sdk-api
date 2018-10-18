---
UID: NS:shobjidl_core.SHELL_ITEM_RESOURCE
title: SHELL_ITEM_RESOURCE
author: windows-sdk-content
description: Defines Shell item resource.
old-location: shell\SHELL_ITEM_RESOURCE.htm
tech.root: shell
ms.assetid: 92ca56a2-e2c3-4651-aa29-115eb07119e9
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: SHELL_ITEM_RESOURCE, SHELL_ITEM_RESOURCE structure [Windows Shell], _shell_SHELL_ITEM_RESOURCE, shell.SHELL_ITEM_RESOURCE, shobjidl_core/SHELL_ITEM_RESOURCE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Shobjidl_core.h
api_name:
 - SHELL_ITEM_RESOURCE
product: Windows
targetos: Windows
req.typenames: SHELL_ITEM_RESOURCE
req.redist: 
---

# SHELL_ITEM_RESOURCE structure


## -description


Defines Shell item resource.


## -struct-fields




### -field guidType

Type: <b>GUID</b>

The <b>GUID</b> that identifies the item.


### -field szName

Type: <b>WCHAR[MAX_PATH]</b>

The item name. A null-terminated Unicode buffer of size MAX_LENGTH characters.

