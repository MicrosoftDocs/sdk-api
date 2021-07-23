---
UID: NF:syncmgr.ISyncMgrSyncItemContainer.GetSyncItemEnumerator
title: ISyncMgrSyncItemContainer::GetSyncItemEnumerator (syncmgr.h)
description: Gets an interface that enumerates the handler's sync items.
helpviewer_keywords: ["GetSyncItemEnumerator","GetSyncItemEnumerator method [Windows Shell]","GetSyncItemEnumerator method [Windows Shell]","ISyncMgrSyncItemContainer interface","ISyncMgrSyncItemContainer interface [Windows Shell]","GetSyncItemEnumerator method","ISyncMgrSyncItemContainer.GetSyncItemEnumerator","ISyncMgrSyncItemContainer::GetSyncItemEnumerator","_shell_ISyncMgrSyncItemContainer_GetSyncItemEnumerator","shell.ISyncMgrSyncItemContainer_GetSyncItemEnumerator","syncmgr/ISyncMgrSyncItemContainer::GetSyncItemEnumerator"]
old-location: shell\ISyncMgrSyncItemContainer_GetSyncItemEnumerator.htm
tech.root: shell
ms.assetid: 761698b8-9531-440e-90f3-41b86f1cc674
ms.date: 12/05/2018
ms.keywords: GetSyncItemEnumerator, GetSyncItemEnumerator method [Windows Shell], GetSyncItemEnumerator method [Windows Shell],ISyncMgrSyncItemContainer interface, ISyncMgrSyncItemContainer interface [Windows Shell],GetSyncItemEnumerator method, ISyncMgrSyncItemContainer.GetSyncItemEnumerator, ISyncMgrSyncItemContainer::GetSyncItemEnumerator, _shell_ISyncMgrSyncItemContainer_GetSyncItemEnumerator, shell.ISyncMgrSyncItemContainer_GetSyncItemEnumerator, syncmgr/ISyncMgrSyncItemContainer::GetSyncItemEnumerator
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
 - ISyncMgrSyncItemContainer::GetSyncItemEnumerator
 - syncmgr/ISyncMgrSyncItemContainer::GetSyncItemEnumerator
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
 - ISyncMgrSyncItemContainer.GetSyncItemEnumerator
---

# ISyncMgrSyncItemContainer::GetSyncItemEnumerator


## -description

Gets an interface that enumerates the handler's sync items.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrsyncitems">IEnumSyncMgrSyncItems</a>**</b>

When this method returns, contains the address of a pointer to an <a href="/windows/desktop/api/syncmgr/nn-syncmgr-ienumsyncmgrsyncitems">IEnumSyncMgrSyncItems</a> instance. <b>IEnumSyncMgrSyncItems</b> can be used to retrieve an interface for each sync item in the set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method replaces the older <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-enumsyncmgritems">EnumSyncMgrItems</a> method. The older method returned an enumerator interface which returned a <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a> structure for each sync item. To get the data previously provided by that structure, Sync Center calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on each item's <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsyncitem">ISyncMgrSyncItem</a> interface to request a corresponding <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsynciteminfo">ISyncMgrSyncItemInfo</a> interface.

The number of enumerated items can be obtained through the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount">ISyncMgrSyncItemContainer::GetSyncItemCount</a> method.


#### Examples

The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetSyncItemEnumerator(
    __out IEnumSyncMgrSyncItems **ppenum)
{
    *ppenum = NULL;

    // Load the items using a private class method.
    HRESULT hr = _LoadItems();

    if (SUCCEEDED(hr))
    {
        hr = CEnumSyncMgrSyncItems_CreateInstance(this,
                                                  IID_PPV_ARGS(ppenum));
    }

    return hr;
}

```