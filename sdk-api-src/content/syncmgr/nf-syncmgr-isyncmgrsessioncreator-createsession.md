---
UID: NF:syncmgr.ISyncMgrSessionCreator.CreateSession
title: ISyncMgrSessionCreator::CreateSession (syncmgr.h)
description: Notifies Sync Center that synchronization of the specified items has begun.
helpviewer_keywords: ["CreateSession","CreateSession method [Windows Shell]","CreateSession method [Windows Shell]","ISyncMgrSessionCreator interface","ISyncMgrSessionCreator interface [Windows Shell]","CreateSession method","ISyncMgrSessionCreator.CreateSession","ISyncMgrSessionCreator::CreateSession","_shell_ISyncMgrSessionCreator_CreateSession","shell.ISyncMgrSessionCreator_CreateSession","syncmgr/ISyncMgrSessionCreator::CreateSession"]
old-location: shell\ISyncMgrSessionCreator_CreateSession.htm
tech.root: shell
ms.assetid: d1df43b6-406c-4da0-89f0-a17e51101520
ms.date: 12/05/2018
ms.keywords: CreateSession, CreateSession method [Windows Shell], CreateSession method [Windows Shell],ISyncMgrSessionCreator interface, ISyncMgrSessionCreator interface [Windows Shell],CreateSession method, ISyncMgrSessionCreator.CreateSession, ISyncMgrSessionCreator::CreateSession, _shell_ISyncMgrSessionCreator_CreateSession, shell.ISyncMgrSessionCreator_CreateSession, syncmgr/ISyncMgrSessionCreator::CreateSession
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
 - ISyncMgrSessionCreator::CreateSession
 - syncmgr/ISyncMgrSessionCreator::CreateSession
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
 - ISyncMgrSessionCreator.CreateSession
---

# ISyncMgrSessionCreator::CreateSession


## -description

Notifies Sync Center that synchronization of the specified items has begun.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param ppszItemIDs [in]

Type: <b>LPCWSTR*</b>

The address of a pointer to a buffer containing an array of item IDs, managed by the handler specified in <i>pszHandlerID</i>, to be synchronized. Each ID is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

### -param cItems [in]

Type: <b>ULONG</b>

The number of item IDs contained in the buffer referenced in <i>ppszItemIDs</i>.

### -param ppCallback [in]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsynccallback">ISyncMgrSyncCallback</a>**</b>

The address of a pointer to an instance of <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsynccallback">ISyncMgrSyncCallback</a> used to report progress and events. This value can be <b>NULL</b> if no callback is needed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Both <i>pszHandlerID</i> and <i>ppszItemIDs</i> must be specified.


#### Examples



The following example shows the outline of an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::Synchronize(...)
{
    ...
    ISyncMgrSyncCallback *pCallback = NULL;

    hr = pCreator->CreateSession(_pszHandlerID, ppszItemIDs, cItems, &pCallback);
    if (SUCCEEDED(hr))
    {
        // Perform synchronization.
    }

    return hr;
}

```