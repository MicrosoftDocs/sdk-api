---
UID: NF:syncmgr.ISyncMgrEventStore.GetEventEnumerator
title: ISyncMgrEventStore::GetEventEnumerator (syncmgr.h)
description: Gets an enumerator for a handler's events.
helpviewer_keywords: ["GetEventEnumerator","GetEventEnumerator method [Windows Shell]","GetEventEnumerator method [Windows Shell]","ISyncMgrEventStore interface","ISyncMgrEventStore interface [Windows Shell]","GetEventEnumerator method","ISyncMgrEventStore.GetEventEnumerator","ISyncMgrEventStore::GetEventEnumerator","_shell_ISyncMgrEventStore_GetEventEnumerator","shell.ISyncMgrEventStore_GetEventEnumerator","syncmgr/ISyncMgrEventStore::GetEventEnumerator"]
old-location: shell\ISyncMgrEventStore_GetEventEnumerator.htm
tech.root: shell
ms.assetid: 8b634811-cb6d-47b2-b534-1baea23a5297
ms.date: 12/05/2018
ms.keywords: GetEventEnumerator, GetEventEnumerator method [Windows Shell], GetEventEnumerator method [Windows Shell],ISyncMgrEventStore interface, ISyncMgrEventStore interface [Windows Shell],GetEventEnumerator method, ISyncMgrEventStore.GetEventEnumerator, ISyncMgrEventStore::GetEventEnumerator, _shell_ISyncMgrEventStore_GetEventEnumerator, shell.ISyncMgrEventStore_GetEventEnumerator, syncmgr/ISyncMgrEventStore::GetEventEnumerator
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
 - ISyncMgrEventStore::GetEventEnumerator
 - syncmgr/ISyncMgrEventStore::GetEventEnumerator
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
 - ISyncMgrEventStore.GetEventEnumerator
---

# ISyncMgrEventStore::GetEventEnumerator


## -description

Gets an enumerator for a handler's events.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrevents">IEnumSyncMgrEvents</a>**</b>

When this method returns, contains the address of a pointer to an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrevents">IEnumSyncMgrEvents</a> instance that can be used to access the handler's events.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by Sync Center when the user navigates to the Sync Results folder or clicks the <b>Errors</b> link for a handler.


#### Examples



The following example shows an implementation of <b>ISyncMgrEventStore::GetEventEnumerator</b>.


```cpp
STDMETHODIMP CMyDeviceEventStore::GetEventEnumerator(
                                __out IEnumSyncMgrEvents **ppenum)
{
    HRESULT hr = CEnumMyDeviceSyncMgrEvents_Create(ppenum);
    return hr;
}

```