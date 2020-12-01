---
UID: NF:syncmgr.FreeConfirmConflictItem
title: FreeConfirmConflictItem function (syncmgr.h)
description: Frees the resources that have been allocated for a CONFIRM_CONFLICT_ITEM structure.
helpviewer_keywords: ["FreeConfirmConflictItem","FreeConfirmConflictItem function [Windows Shell]","_shell_FreeConfirmConflictItem","shell.FreeConfirmConflictItem","syncmgr/FreeConfirmConflictItem"]
old-location: shell\FreeConfirmConflictItem.htm
tech.root: shell
ms.assetid: 504a63e0-39e9-4228-ab3d-c34b272f8fd3
ms.date: 12/05/2018
ms.keywords: FreeConfirmConflictItem, FreeConfirmConflictItem function [Windows Shell], _shell_FreeConfirmConflictItem, shell.FreeConfirmConflictItem, syncmgr/FreeConfirmConflictItem
req.header: syncmgr.h
req.include-header: Syncmgr.idl
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: None
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeConfirmConflictItem
 - syncmgr/FreeConfirmConflictItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - FreeConfirmConflictItem
---

# FreeConfirmConflictItem function


## -description

Frees the resources that have been allocated for a <a href="/windows/desktop/api/syncmgr/ns-syncmgr-confirm_conflict_item">CONFIRM_CONFLICT_ITEM</a> structure.

## -parameters

### -param pcci [in, out]

Type: <b><a href="/windows/desktop/api/syncmgr/ns-syncmgr-confirm_conflict_item">CONFIRM_CONFLICT_ITEM</a>*</b>

A pointer to a <a href="/windows/desktop/api/syncmgr/ns-syncmgr-confirm_conflict_item">CONFIRM_CONFLICT_ITEM</a> structure that stores pointers to the items for which memory is to be freed.