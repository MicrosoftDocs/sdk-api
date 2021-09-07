---
UID: NF:syncmgr.ISyncMgrControl.StartSyncAll
title: ISyncMgrControl::StartSyncAll (syncmgr.h)
description: Synchronizes all items managed by all handlers.
helpviewer_keywords: ["ISyncMgrControl interface [Windows Shell]","StartSyncAll method","ISyncMgrControl.StartSyncAll","ISyncMgrControl::StartSyncAll","StartSyncAll","StartSyncAll method [Windows Shell]","StartSyncAll method [Windows Shell]","ISyncMgrControl interface","_shell_ISyncMgrControl_StartSyncAll","shell.ISyncMgrControl_StartSyncAll","syncmgr/ISyncMgrControl::StartSyncAll"]
old-location: shell\ISyncMgrControl_StartSyncAll.htm
tech.root: shell
ms.assetid: 3b0d5070-1866-4346-b2bf-93b48a952af6
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],StartSyncAll method, ISyncMgrControl.StartSyncAll, ISyncMgrControl::StartSyncAll, StartSyncAll, StartSyncAll method [Windows Shell], StartSyncAll method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_StartSyncAll, shell.ISyncMgrControl_StartSyncAll, syncmgr/ISyncMgrControl::StartSyncAll
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
 - ISyncMgrControl::StartSyncAll
 - syncmgr/ISyncMgrControl::StartSyncAll
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
 - ISyncMgrControl.StartSyncAll
---

# ISyncMgrControl::StartSyncAll


## -description

Synchronizes all items managed by all handlers.

## -parameters

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to a window that can be used by a handler or item to display any necessary UI. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is analogous to <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateall">UpdateAll</a>.


#### Examples



The following example shows the usage of <b>ISyncMgrControl::StartSyncAll</b> by a handler's procedure.


```cpp
void CMyDeviceHandler::MiscProc(...)
{
    ...

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER,
                          IID_PPV_ARGS(&pControl));
    if (SUCCEEDED(hr))
    {
        // Synchronize all sync items for all sync handlers.
        hr = pControl->StartSyncAll(_hwnd);
        pControl->Release();
    }

    ...

}

```