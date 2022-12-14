---
UID: NF:syncmgr.ISyncMgrConflictItems.GetItem
title: ISyncMgrConflictItems::GetItem (syncmgr.h)
description: Gets a specified conflict data item.
helpviewer_keywords: ["GetItem","GetItem method [Windows Shell]","GetItem method [Windows Shell]","ISyncMgrConflictItems interface","ISyncMgrConflictItems interface [Windows Shell]","GetItem method","ISyncMgrConflictItems.GetItem","ISyncMgrConflictItems::GetItem","_shell_ISyncMgrConflictItems_GetItem","shell.ISyncMgrConflictItems_GetItem","syncmgr/ISyncMgrConflictItems::GetItem"]
old-location: shell\ISyncMgrConflictItems_GetItem.htm
tech.root: shell
ms.assetid: f75a0cc5-1f82-426a-bb66-f34000219300
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Shell], GetItem method [Windows Shell],ISyncMgrConflictItems interface, ISyncMgrConflictItems interface [Windows Shell],GetItem method, ISyncMgrConflictItems.GetItem, ISyncMgrConflictItems::GetItem, _shell_ISyncMgrConflictItems_GetItem, shell.ISyncMgrConflictItems_GetItem, syncmgr/ISyncMgrConflictItems::GetItem
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrConflictItems::GetItem
 - syncmgr/ISyncMgrConflictItems::GetItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrConflictItems.GetItem
---

# ISyncMgrConflictItems::GetItem


## -description

Gets a specified conflict data item.

## -parameters

### -param iIndex [in]

Type: <b>UINT</b>

The index of the conflict item to retrieve.

### -param pItemInfo [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ns-syncmgr-confirm_conflict_item">CONFIRM_CONFLICT_ITEM</a>*</b>

When this method returns successfully, contains a pointer to a <a href="/windows/desktop/api/syncmgr/ns-syncmgr-confirm_conflict_item">CONFIRM_CONFLICT_ITEM</a> structure that contains information about the conflict.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.