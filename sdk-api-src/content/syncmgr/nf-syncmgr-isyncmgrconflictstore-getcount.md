---
UID: NF:syncmgr.ISyncMgrConflictStore.GetCount
title: ISyncMgrConflictStore::GetCount (syncmgr.h)
description: Gets the number of conflicts in the store.
helpviewer_keywords: ["GetCount","GetCount method [Windows Shell]","GetCount method [Windows Shell]","ISyncMgrConflictStore interface","ISyncMgrConflictStore interface [Windows Shell]","GetCount method","ISyncMgrConflictStore.GetCount","ISyncMgrConflictStore::GetCount","_shell_ISyncMgrConflictStore_GetCount","shell.ISyncMgrConflictStore_GetCount","syncmgr/ISyncMgrConflictStore::GetCount"]
old-location: shell\ISyncMgrConflictStore_GetCount.htm
tech.root: shell
ms.assetid: 1a41bc9a-6f5d-47bf-9186-711292d8be07
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],ISyncMgrConflictStore interface, ISyncMgrConflictStore interface [Windows Shell],GetCount method, ISyncMgrConflictStore.GetCount, ISyncMgrConflictStore::GetCount, _shell_ISyncMgrConflictStore_GetCount, shell.ISyncMgrConflictStore_GetCount, syncmgr/ISyncMgrConflictStore::GetCount
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
 - ISyncMgrConflictStore::GetCount
 - syncmgr/ISyncMgrConflictStore::GetCount
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
 - ISyncMgrConflictStore.GetCount
---

# ISyncMgrConflictStore::GetCount


## -description

Gets the number of conflicts in the store.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a sync handler ID as a Unicode string.

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a sync item ID as a Unicode string.

### -param pnConflicts [out]

Type: <b>DWORD*</b>

When this method returns, contains the conflict count.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

