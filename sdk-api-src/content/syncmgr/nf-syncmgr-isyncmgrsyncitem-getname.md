---
UID: NF:syncmgr.ISyncMgrSyncItem.GetName
title: ISyncMgrSyncItem::GetName (syncmgr.h)
description: Gets the UI display name of the sync item.
helpviewer_keywords: ["GetName","GetName method [Windows Shell]","GetName method [Windows Shell]","ISyncMgrSyncItem interface","ISyncMgrSyncItem interface [Windows Shell]","GetName method","ISyncMgrSyncItem.GetName","ISyncMgrSyncItem::GetName","_shell_ISyncMgrSyncItem_GetName","shell.ISyncMgrSyncItem_GetName","syncmgr/ISyncMgrSyncItem::GetName"]
old-location: shell\ISyncMgrSyncItem_GetName.htm
tech.root: shell
ms.assetid: 4a5f8430-7b5a-4184-acc9-ae4395acf2fa
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Windows Shell], GetName method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetName method, ISyncMgrSyncItem.GetName, ISyncMgrSyncItem::GetName, _shell_ISyncMgrSyncItem_GetName, shell.ISyncMgrSyncItem_GetName, syncmgr/ISyncMgrSyncItem::GetName
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
 - ISyncMgrSyncItem::GetName
 - syncmgr/ISyncMgrSyncItem::GetName
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
 - ISyncMgrSyncItem.GetName
---

# ISyncMgrSyncItem::GetName


## -description

Gets the UI display name of the sync item.

## -parameters

### -param ppszName [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the item's display name. This string is of maximum length MAX_SYNCMGR_NAME including the terminating <b>null</b> character. Longer strings are truncated.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <b>GetName</b> fails or an empty string is returned in <i>ppszItemID</i>, the sync item is not shown in the handler's folder and Sync Center will not attempt to synchronize it.

The ID retrieved by this method is available in the handler's folder UI as the System.DisplayName (PKEY_DisplayName) property.

The item is responsible for allocating the string buffer pointed to by <i>ppszComment</i> through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateitem">UpdateItem</a> method is called.

In older Sync Manager implementations, this information was retrieved through the <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrhandlerinfo">SYNCMGRHANDLERINFO</a> structure.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceSyncItem::GetName(__out LPWSTR *ppszName)
{
    *ppszName = NULL;
    HRESULT hr = SHCoAllocString(_pszItemName, ppszName);
    return hr;
}

```