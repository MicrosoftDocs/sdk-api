---
UID: NS:syncmgr.CONFIRM_CONFLICT_ITEM
title: CONFIRM_CONFLICT_ITEM (syncmgr.h)
author: windows-sdk-content
description: Defines conflict item structure.
old-location: shell\CONFIRM_CONFLICT_ITEM.htm
tech.root: shell
ms.assetid: 3be4a8ec-eeab-4453-a2cb-18cadf39464a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CONFIRM_CONFLICT_ITEM, CONFIRM_CONFLICT_ITEM structure [Windows Shell], _shell_CONFIRM_CONFLICT_ITEM, shell.CONFIRM_CONFLICT_ITEM, syncmgr/CONFIRM_CONFLICT_ITEM
ms.topic: struct
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - Syncmgr.h
api_name:
 - CONFIRM_CONFLICT_ITEM
product: Windows
targetos: Windows
req.typenames: CONFIRM_CONFLICT_ITEM
req.redist: 
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

