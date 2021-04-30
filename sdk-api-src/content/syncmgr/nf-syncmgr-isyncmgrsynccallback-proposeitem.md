---
UID: NF:syncmgr.ISyncMgrSyncCallback.ProposeItem
title: ISyncMgrSyncCallback::ProposeItem (syncmgr.h)
description: Proposes the addition of a new item to the set of items previously enumerated.
helpviewer_keywords: ["ISyncMgrSyncCallback interface [Windows Shell]","ProposeItem method","ISyncMgrSyncCallback.ProposeItem","ISyncMgrSyncCallback::ProposeItem","ProposeItem","ProposeItem method [Windows Shell]","ProposeItem method [Windows Shell]","ISyncMgrSyncCallback interface","_shell_ISyncMgrSyncCallback_ProposeItem","shell.ISyncMgrSyncCallback_ProposeItem","syncmgr/ISyncMgrSyncCallback::ProposeItem"]
old-location: shell\ISyncMgrSyncCallback_ProposeItem.htm
tech.root: shell
ms.assetid: d0c73950-f80e-4831-9c56-4316561a269b
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncCallback interface [Windows Shell],ProposeItem method, ISyncMgrSyncCallback.ProposeItem, ISyncMgrSyncCallback::ProposeItem, ProposeItem, ProposeItem method [Windows Shell], ProposeItem method [Windows Shell],ISyncMgrSyncCallback interface, _shell_ISyncMgrSyncCallback_ProposeItem, shell.ISyncMgrSyncCallback_ProposeItem, syncmgr/ISyncMgrSyncCallback::ProposeItem
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
 - ISyncMgrSyncCallback::ProposeItem
 - syncmgr/ISyncMgrSyncCallback::ProposeItem
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
 - ISyncMgrSyncCallback.ProposeItem
---

# ISyncMgrSyncCallback::ProposeItem


## -description

Proposes the addition of a new item to the set of items previously enumerated.

## -parameters

### -param pNewItem [in]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a>*</b>

A pointer to an instance of <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a> representing the new item.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns E_INVALIDARG if <i>pszItemID</i> already exists.

## -remarks

<b>ISyncMgrSyncCallback::ProposeItem</b> is typically called when items are not considered part of the sync set unless they have been successfully synchronized. Sync Center does not display this item in the UI until the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-commititem">ISyncMgrSyncCallback::CommitItem</a> method has been called.


#### Examples



The following example shows the usage of <b>ISyncMgrSyncCallback::ProposeItem</b> and <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-commititem">ISyncMgrSyncCallback::CommitItem</a> by the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">Synchronize</a> method.


```cpp
HRESULT CMyDeviceHandler::Synchronize(...)
{
    ...

    // Start synchronizing the handler.

    ...

    // Find items waiting to be created.
    for (...)
    {
        // Create the item.
        ISyncMgrSyncItem *pNewItem = NULL;
        LPWSTR szItemID[MAX_SYNCMGR_ID];
        
        hr = GetNextNewItem(&pNewItem, szItemID, ARRAYSIZE(szItemID));
        if (SUCCEEDED(hr))
        {
            // Propose this item to Sync Center.
            hr = pCallback->ProposeItem(pNewItem);
            if (SUCCEEDED(hr))
            {
                // Synchronize the item.
                // Synchronization was successful.  Commit the item.
                hr = pCallback->CommitItem(szItemID);
            }
            pNewItem->Release();
        }
    }
    ...
}

```