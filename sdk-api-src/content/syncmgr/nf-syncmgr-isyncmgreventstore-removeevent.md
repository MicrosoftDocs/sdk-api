---
UID: NF:syncmgr.ISyncMgrEventStore.RemoveEvent
title: ISyncMgrEventStore::RemoveEvent (syncmgr.h)
description: Removes events, as specified.
helpviewer_keywords: ["ISyncMgrEventStore interface [Windows Shell]","RemoveEvent method","ISyncMgrEventStore.RemoveEvent","ISyncMgrEventStore::RemoveEvent","RemoveEvent","RemoveEvent method [Windows Shell]","RemoveEvent method [Windows Shell]","ISyncMgrEventStore interface","_shell_ISyncMgrEventStore_RemoveEvent","shell.ISyncMgrEventStore_RemoveEvent","syncmgr/ISyncMgrEventStore::RemoveEvent"]
old-location: shell\ISyncMgrEventStore_RemoveEvent.htm
tech.root: shell
ms.assetid: 08d01b6f-1e1f-4f03-9595-f374805ae734
ms.date: 12/05/2018
ms.keywords: ISyncMgrEventStore interface [Windows Shell],RemoveEvent method, ISyncMgrEventStore.RemoveEvent, ISyncMgrEventStore::RemoveEvent, RemoveEvent, RemoveEvent method [Windows Shell], RemoveEvent method [Windows Shell],ISyncMgrEventStore interface, _shell_ISyncMgrEventStore_RemoveEvent, shell.ISyncMgrEventStore_RemoveEvent, syncmgr/ISyncMgrEventStore::RemoveEvent
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
 - ISyncMgrEventStore::RemoveEvent
 - syncmgr/ISyncMgrEventStore::RemoveEvent
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
 - ISyncMgrEventStore.RemoveEvent
---

# ISyncMgrEventStore::RemoveEvent


## -description

Removes events, as specified.

## -parameters

### -param pguidEventIDs [in]

Type: <b>GUID*</b>

A pointer to event <b>GUID</b>.

### -param cEvents [in]

Type: <b>ULONG</b>

The count of events to remove.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

