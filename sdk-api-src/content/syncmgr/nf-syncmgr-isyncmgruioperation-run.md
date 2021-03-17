---
UID: NF:syncmgr.ISyncMgrUIOperation.Run
title: ISyncMgrUIOperation::Run (syncmgr.h)
description: Performs the actual display of UI for a handler or sync item when requested to do so by Sync Center.
helpviewer_keywords: ["ISyncMgrUIOperation interface [Windows Shell]","Run method","ISyncMgrUIOperation.Run","ISyncMgrUIOperation::Run","Run","Run method [Windows Shell]","Run method [Windows Shell]","ISyncMgrUIOperation interface","_shell_ISyncMgrUIOperation_Run","shell.ISyncMgrUIOperation_Run","syncmgr/ISyncMgrUIOperation::Run"]
old-location: shell\ISyncMgrUIOperation_Run.htm
tech.root: shell
ms.assetid: 66dd853e-0fb0-4736-982a-e0183cb51842
ms.date: 12/05/2018
ms.keywords: ISyncMgrUIOperation interface [Windows Shell],Run method, ISyncMgrUIOperation.Run, ISyncMgrUIOperation::Run, Run, Run method [Windows Shell], Run method [Windows Shell],ISyncMgrUIOperation interface, _shell_ISyncMgrUIOperation_Run, shell.ISyncMgrUIOperation_Run, syncmgr/ISyncMgrUIOperation::Run
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
 - ISyncMgrUIOperation::Run
 - syncmgr/ISyncMgrUIOperation::Run
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
 - ISyncMgrUIOperation.Run
---

# ISyncMgrUIOperation::Run


## -description

Performs the actual display of UI for a handler or sync item when requested to do so by Sync Center.

## -parameters

### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the window used to display the UI.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns S_FALSE or another error code if this method is called to confirm an operation, such as activating a handler or disabling a sync item, but that operation should not be executed.

## -remarks

The handler itself, not the UI, is expected to use the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrcontrol">ISyncMgrControl</a> interface to notify Sync Center of changes to its state that come about through choices made by the user in the UI.


#### Examples



The following example shows the outline of an implementation of this method. In this case, the implementation is that which would be returned when <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">GetObject</a> is called with the SYNCMGR_OBJECTID_QueryBeforeDelete object ID.


```cpp
STDMETHODIMP CQueryBeforeDelete::Run(__in HWND hwndOwner)
{
    HRESULT hr = S_OK;

    // Display a dialog confirming that the user wants to delete the item.

    return hr;
}

```