---
UID: NF:syncmgr.IEnumSyncMgrSyncItems.Next
title: IEnumSyncMgrSyncItems::Next (syncmgr.h)
description: Gets the next batch of sync items from the handler.
helpviewer_keywords: ["IEnumSyncMgrSyncItems interface [Windows Shell]","Next method","IEnumSyncMgrSyncItems.Next","IEnumSyncMgrSyncItems::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumSyncMgrSyncItems interface","_shell_IEnumSyncMgrSyncItems_Next","shell.IEnumSyncMgrSyncItems_Next","syncmgr/IEnumSyncMgrSyncItems::Next"]
old-location: shell\IEnumSyncMgrSyncItems_Next.htm
tech.root: shell
ms.assetid: b886e3a8-a94b-45ed-893b-889bef70ae6a
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrSyncItems interface [Windows Shell],Next method, IEnumSyncMgrSyncItems.Next, IEnumSyncMgrSyncItems::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumSyncMgrSyncItems interface, _shell_IEnumSyncMgrSyncItems_Next, shell.IEnumSyncMgrSyncItems_Next, syncmgr/IEnumSyncMgrSyncItems::Next
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
 - IEnumSyncMgrSyncItems::Next
 - syncmgr/IEnumSyncMgrSyncItems::Next
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
 - IEnumSyncMgrSyncItems.Next
---

# IEnumSyncMgrSyncItems::Next


## -description

Gets the next batch of sync items from the handler.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

This value must be 1.

### -param rgelt [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a>**</b>

The address of an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a> interface pointer.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of items fetched.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.