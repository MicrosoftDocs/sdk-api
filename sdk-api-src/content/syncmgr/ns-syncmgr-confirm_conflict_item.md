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

# CONFIRM_CONFLICT_ITEM structure


## -description


Defines conflict item structure.


## -struct-fields




### -field pShellItem

Type: <b><a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>*</b>

A pointer to <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a> interface.


### -field pszOriginalName

Type: <b>LPWSTR</b>

A pointer to the original name. If set to <b>NULL</b> then IShellItem's display name will be used.


### -field pszAlternateName

Type: <b>LPWSTR</b>

A pointer to the alternate name. If multiple items are kept, then item must be renamed to this name. User may or may not have an ability to change the name.


### -field pszLocationShort

Type: <b>LPWSTR</b>

A pointer to the short location.


### -field pszLocationFull

Type: <b>LPWSTR</b>

A pointer to the full location.


### -field nType

Type: <b><a href="https://msdn.microsoft.com/b0bc2285-b3a3-43a9-b169-611f587bb086">SYNCMGR_CONFLICT_ITEM_TYPE</a></b>

The conflict item type. See <a href="https://msdn.microsoft.com/b0bc2285-b3a3-43a9-b169-611f587bb086">SYNCMGR_CONFLICT_ITEM_TYPE</a>.

