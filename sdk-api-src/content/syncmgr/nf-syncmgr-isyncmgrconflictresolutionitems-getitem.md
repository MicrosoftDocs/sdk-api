---
UID: NF:syncmgr.ISyncMgrConflictResolutionItems.GetItem
title: ISyncMgrConflictResolutionItems::GetItem (syncmgr.h)
description: Gets result information for a specified item, when successful.
helpviewer_keywords: ["GetItem","GetItem method [Windows Shell]","GetItem method [Windows Shell]","ISyncMgrConflictResolutionItems interface","ISyncMgrConflictResolutionItems interface [Windows Shell]","GetItem method","ISyncMgrConflictResolutionItems.GetItem","ISyncMgrConflictResolutionItems::GetItem","_shell_ISyncMgrConflictResolutionItems_GetItem","shell.ISyncMgrConflictResolutionItems_GetItem","syncmgr/ISyncMgrConflictResolutionItems::GetItem"]
old-location: shell\ISyncMgrConflictResolutionItems_GetItem.htm
tech.root: shell
ms.assetid: c98ec4fa-bbca-4213-95c3-b50ccafbbfdb
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Shell], GetItem method [Windows Shell],ISyncMgrConflictResolutionItems interface, ISyncMgrConflictResolutionItems interface [Windows Shell],GetItem method, ISyncMgrConflictResolutionItems.GetItem, ISyncMgrConflictResolutionItems::GetItem, _shell_ISyncMgrConflictResolutionItems_GetItem, shell.ISyncMgrConflictResolutionItems_GetItem, syncmgr/ISyncMgrConflictResolutionItems::GetItem
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
 - ISyncMgrConflictResolutionItems::GetItem
 - syncmgr/ISyncMgrConflictResolutionItems::GetItem
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
 - ISyncMgrConflictResolutionItems.GetItem
---

# ISyncMgrConflictResolutionItems::GetItem


## -description

Gets result information for a specified item, when successful.

## -parameters

### -param iIndex [in]

Type: <b>UINT</b>

The index of the item.

### -param pItemInfo [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ns-syncmgr-confirm_conflict_result_info">CONFIRM_CONFLICT_RESULT_INFO</a>*</b>

On success, contains a pointer to a <a href="/windows/desktop/api/syncmgr/ns-syncmgr-confirm_conflict_result_info">CONFIRM_CONFLICT_RESULT_INFO</a> structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.