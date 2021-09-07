---
UID: NF:syncmgr.ISyncMgrConflictStore.BindToConflict
title: ISyncMgrConflictStore::BindToConflict (syncmgr.h)
description: Binds to a particular conflict specified by IID.
helpviewer_keywords: ["BindToConflict","BindToConflict method [Windows Shell]","BindToConflict method [Windows Shell]","ISyncMgrConflictStore interface","ISyncMgrConflictStore interface [Windows Shell]","BindToConflict method","ISyncMgrConflictStore.BindToConflict","ISyncMgrConflictStore::BindToConflict","_shell_ISyncMgrConflictStore_BindToConflict","shell.ISyncMgrConflictStore_BindToConflict","syncmgr/ISyncMgrConflictStore::BindToConflict"]
old-location: shell\ISyncMgrConflictStore_BindToConflict.htm
tech.root: shell
ms.assetid: 86414360-7dc5-4819-8372-0cede07ba41b
ms.date: 12/05/2018
ms.keywords: BindToConflict, BindToConflict method [Windows Shell], BindToConflict method [Windows Shell],ISyncMgrConflictStore interface, ISyncMgrConflictStore interface [Windows Shell],BindToConflict method, ISyncMgrConflictStore.BindToConflict, ISyncMgrConflictStore::BindToConflict, _shell_ISyncMgrConflictStore_BindToConflict, shell.ISyncMgrConflictStore_BindToConflict, syncmgr/ISyncMgrConflictStore::BindToConflict
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
 - ISyncMgrConflictStore::BindToConflict
 - syncmgr/ISyncMgrConflictStore::BindToConflict
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
 - ISyncMgrConflictStore.BindToConflict
---

# ISyncMgrConflictStore::BindToConflict


## -description

Binds to a particular conflict specified by IID.

## -parameters

### -param pConflictIdInfo [in]

Type: <b>const <a href="/windows/desktop/api/syncmgr/ns-syncmgr-syncmgr_conflict_id_info">SYNCMGR_CONFLICT_ID_INFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/syncmgr/ns-syncmgr-syncmgr_conflict_id_info">SYNCMGR_CONFLICT_ID_INFO</a> structure.

### -param riid [in]

Type: <b>REFIID</b>

A reference to a desired conflict IID.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used when the conflict folder binds to a conflict, given its pointer to an item identifier list (PIDL) or parsing name. The ID is obtained from a conflict that was previously extracted from the store. See <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflict">ISyncMgrConflict</a>.