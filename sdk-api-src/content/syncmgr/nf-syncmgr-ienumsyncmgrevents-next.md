---
UID: NF:syncmgr.IEnumSyncMgrEvents.Next
title: IEnumSyncMgrEvents::Next (syncmgr.h)
description: Gets the next batch of events from the event store.
helpviewer_keywords: ["IEnumSyncMgrEvents interface [Windows Shell]","Next method","IEnumSyncMgrEvents.Next","IEnumSyncMgrEvents::Next","Next","Next method [Windows Shell]","Next method [Windows Shell]","IEnumSyncMgrEvents interface","_shell_IEnumSyncMgrEvents_Next","shell.IEnumSyncMgrEvents_Next","syncmgr/IEnumSyncMgrEvents::Next"]
old-location: shell\IEnumSyncMgrEvents_Next.htm
tech.root: shell
ms.assetid: 22151b04-f4b8-46af-b55a-1ac2054900d3
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrEvents interface [Windows Shell],Next method, IEnumSyncMgrEvents.Next, IEnumSyncMgrEvents::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumSyncMgrEvents interface, _shell_IEnumSyncMgrEvents_Next, shell.IEnumSyncMgrEvents_Next, syncmgr/IEnumSyncMgrEvents::Next
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
 - IEnumSyncMgrEvents::Next
 - syncmgr/IEnumSyncMgrEvents::Next
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
 - IEnumSyncMgrEvents.Next
---

# IEnumSyncMgrEvents::Next


## -description

Gets the next batch of events from the event store.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

This value must be 1.

### -param rgelt [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a>**</b>

The address of an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a> interface pointer.

### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of events fetched.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.