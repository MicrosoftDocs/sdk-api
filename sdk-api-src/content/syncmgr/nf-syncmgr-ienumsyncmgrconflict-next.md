---
UID: NF:syncmgr.IEnumSyncMgrConflict.Next
title: IEnumSyncMgrConflict::Next (syncmgr.h)
description: Gets the next batch of conflicts from the conflicts store.
helpviewer_keywords: ["IEnumSyncMgrConflict interface [Windows Shell]","Next method","IEnumSyncMgrConflict.Next","IEnumSyncMgrConflict::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumSyncMgrConflict interface","_shell_IEnumSyncMgrConflict_Next","shell.IEnumSyncMgrConflict_Next","syncmgr/IEnumSyncMgrConflict::Next"]
old-location: shell\IEnumSyncMgrConflict_Next.htm
tech.root: shell
ms.assetid: 486fba93-cdd1-49fd-96a8-cf56d1775a7c
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrConflict interface [Windows Shell],Next method, IEnumSyncMgrConflict.Next, IEnumSyncMgrConflict::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumSyncMgrConflict interface, _shell_IEnumSyncMgrConflict_Next, shell.IEnumSyncMgrConflict_Next, syncmgr/IEnumSyncMgrConflict::Next
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
 - IEnumSyncMgrConflict::Next
 - syncmgr/IEnumSyncMgrConflict::Next
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
 - IEnumSyncMgrConflict.Next
---

# IEnumSyncMgrConflict::Next


## -description

Gets the next batch of conflicts from the conflicts store.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

The value must be 1.

### -param rgelt [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflict">ISyncMgrConflict</a>**</b>

The address of an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflict">ISyncMgrConflict</a> interface pointer.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of conflicts fetched.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.