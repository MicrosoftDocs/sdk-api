---
UID: NF:syncmgr.ISyncMgrEventStore.GetEvent
title: ISyncMgrEventStore::GetEvent (syncmgr.h)
description: Gets a specified event object.
helpviewer_keywords: ["GetEvent","GetEvent method [Windows Shell]","GetEvent method [Windows Shell]","ISyncMgrEventStore interface","ISyncMgrEventStore interface [Windows Shell]","GetEvent method","ISyncMgrEventStore.GetEvent","ISyncMgrEventStore::GetEvent","_shell_ISyncMgrEventStore_GetEvent","shell.ISyncMgrEventStore_GetEvent","syncmgr/ISyncMgrEventStore::GetEvent"]
old-location: shell\ISyncMgrEventStore_GetEvent.htm
tech.root: shell
ms.assetid: 6800ac62-1fd5-43a4-bd37-831449274a7b
ms.date: 12/05/2018
ms.keywords: GetEvent, GetEvent method [Windows Shell], GetEvent method [Windows Shell],ISyncMgrEventStore interface, ISyncMgrEventStore interface [Windows Shell],GetEvent method, ISyncMgrEventStore.GetEvent, ISyncMgrEventStore::GetEvent, _shell_ISyncMgrEventStore_GetEvent, shell.ISyncMgrEventStore_GetEvent, syncmgr/ISyncMgrEventStore::GetEvent
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
 - ISyncMgrEventStore::GetEvent
 - syncmgr/ISyncMgrEventStore::GetEvent
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
 - ISyncMgrEventStore.GetEvent
---

# ISyncMgrEventStore::GetEvent


## -description

Gets a specified event object.

## -parameters

### -param rguidEventID [in]

Type: <b>REFGUID</b>

A reference to event <b>GUID</b>.

### -param ppEvent [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a>**</b>

The address of <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.