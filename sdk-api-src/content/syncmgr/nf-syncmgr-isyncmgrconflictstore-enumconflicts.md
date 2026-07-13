---
UID: NF:syncmgr.ISyncMgrConflictStore.EnumConflicts
title: ISyncMgrConflictStore::EnumConflicts (syncmgr.h)
description: Enumerates conflicts scoped to the provided sync handler and sync item.
helpviewer_keywords: ["EnumConflicts","EnumConflicts method [Windows Shell]","EnumConflicts method [Windows Shell]","ISyncMgrConflictStore interface","ISyncMgrConflictStore interface [Windows Shell]","EnumConflicts method","ISyncMgrConflictStore.EnumConflicts","ISyncMgrConflictStore::EnumConflicts","_shell_ISyncMgrConflictStore_EnumConflicts","shell.ISyncMgrConflictStore_EnumConflicts","syncmgr/ISyncMgrConflictStore::EnumConflicts"]
old-location: shell\ISyncMgrConflictStore_EnumConflicts.htm
tech.root: shell
ms.assetid: b59c679c-7759-4b7a-9a23-f054af99d6a7
ms.date: 12/05/2018
ms.keywords: EnumConflicts, EnumConflicts method [Windows Shell], EnumConflicts method [Windows Shell],ISyncMgrConflictStore interface, ISyncMgrConflictStore interface [Windows Shell],EnumConflicts method, ISyncMgrConflictStore.EnumConflicts, ISyncMgrConflictStore::EnumConflicts, _shell_ISyncMgrConflictStore_EnumConflicts, shell.ISyncMgrConflictStore_EnumConflicts, syncmgr/ISyncMgrConflictStore::EnumConflicts
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
 - ISyncMgrConflictStore::EnumConflicts
 - syncmgr/ISyncMgrConflictStore::EnumConflicts
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
 - ISyncMgrConflictStore.EnumConflicts
---

# ISyncMgrConflictStore::EnumConflicts


## -description

Enumerates conflicts scoped to the provided sync handler and sync item.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to the sync handler ID as a Unicode string.

### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to the sync item ID as a Unicode string.

### -param ppEnum [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrconflict">IEnumSyncMgrConflict</a>**</b>

The address of an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrconflict">IEnumSyncMgrConflict</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the sync handler, sync item, or partner name is <b>NULL</b>, the conflict store ignores that parameter.