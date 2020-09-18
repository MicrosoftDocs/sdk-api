---
UID: NF:syncmgr.ISyncMgrSyncCallback.CommitItem
title: ISyncMgrSyncCallback::CommitItem (syncmgr.h)
description: Confirms a specified item as a member of the handler's sync set and confirms that it should be shown in the UI.
helpviewer_keywords: ["CommitItem","CommitItem method [Windows Shell]","CommitItem method [Windows Shell]","ISyncMgrSyncCallback interface","ISyncMgrSyncCallback interface [Windows Shell]","CommitItem method","ISyncMgrSyncCallback.CommitItem","ISyncMgrSyncCallback::CommitItem","_shell_ISyncMgrSyncCallback_CommitItem","shell.ISyncMgrSyncCallback_CommitItem","syncmgr/ISyncMgrSyncCallback::CommitItem"]
old-location: shell\ISyncMgrSyncCallback_CommitItem.htm
tech.root: shell
ms.assetid: e0964cd3-42ad-4af0-90b2-0f365f457448
ms.date: 12/05/2018
ms.keywords: CommitItem, CommitItem method [Windows Shell], CommitItem method [Windows Shell],ISyncMgrSyncCallback interface, ISyncMgrSyncCallback interface [Windows Shell],CommitItem method, ISyncMgrSyncCallback.CommitItem, ISyncMgrSyncCallback::CommitItem, _shell_ISyncMgrSyncCallback_CommitItem, shell.ISyncMgrSyncCallback_CommitItem, syncmgr/ISyncMgrSyncCallback::CommitItem
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
 - ISyncMgrSyncCallback::CommitItem
 - syncmgr/ISyncMgrSyncCallback::CommitItem
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
 - ISyncMgrSyncCallback.CommitItem
---

# ISyncMgrSyncCallback::CommitItem


## -description

Confirms a specified item as a member of the handler's sync set and confirms that it should be shown in the UI.

## -parameters

### -param pszItemID [in]

Type: <b>LPCWSTR*</b>

A pointer to a buffer containing the unique ID of the item to confirm. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns E_INVALIDARG if the item has not been first submitted through <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-proposeitem">ISyncMgrSyncCallback::ProposeItem</a> or if the item is already part of the current session.