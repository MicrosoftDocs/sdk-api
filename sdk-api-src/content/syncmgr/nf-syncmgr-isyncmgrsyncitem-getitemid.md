---
UID: NF:syncmgr.ISyncMgrSyncItem.GetItemID
title: ISyncMgrSyncItem::GetItemID (syncmgr.h)
description: Gets the unique ID of a sync item.
helpviewer_keywords: ["GetItemID","GetItemID method [Windows Shell]","GetItemID method [Windows Shell]","ISyncMgrSyncItem interface","ISyncMgrSyncItem interface [Windows Shell]","GetItemID method","ISyncMgrSyncItem.GetItemID","ISyncMgrSyncItem::GetItemID","_shell_ISyncMgrSyncItem_GetItemID","shell.ISyncMgrSyncItem_GetItemID","syncmgr/ISyncMgrSyncItem::GetItemID"]
old-location: shell\ISyncMgrSyncItem_GetItemID.htm
tech.root: shell
ms.assetid: 2add1902-1258-49ed-ad44-35d28d0776c1
ms.date: 12/05/2018
ms.keywords: GetItemID, GetItemID method [Windows Shell], GetItemID method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetItemID method, ISyncMgrSyncItem.GetItemID, ISyncMgrSyncItem::GetItemID, _shell_ISyncMgrSyncItem_GetItemID, shell.ISyncMgrSyncItem_GetItemID, syncmgr/ISyncMgrSyncItem::GetItemID
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
 - ISyncMgrSyncItem::GetItemID
 - syncmgr/ISyncMgrSyncItem::GetItemID
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
 - ISyncMgrSyncItem.GetItemID
---

# ISyncMgrSyncItem::GetItemID


## -description

Gets the unique ID of a sync item.

## -parameters

### -param ppszItemID [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the item's ID. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The ID retrieved by this method cannot change. Typically, the ID is in the form of a GUID string. However, this is not a requirement. The ID can be any string that is unique in the context of the handler.

If <b>GetItemID</b> fails or an empty string is returned in <i>ppszItemID</i>, the sync item is not shown in the handler's folder and Sync Center will not attempt to synchronize it.

The ID retrieved by this method is available in the folder UI as the System.Sync.ItemID (PKEY_Sync_HandlerID) property.

The item is responsible for allocating the string buffer pointed to by <i>ppszComment</i> through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

In older Sync Manager implementations, this data was retrieved through the <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a> structure.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceSyncItem::GetItemID(__out LPWSTR *ppszItemID)
{
    HRESULT hr = S_OK;
    *ppszName = NULL;

    // Generate the string version of the ID.
    if (_pszItemID == NULL)
    {
        LPOLESTR pszItemID = NULL;
        hr = StringFromCLSID(_guidItemID, &_pszItemID);
    }

    if (SUCCEEDED(hr))
    {
        // Duplicate the item ID string for the caller.
        hr = SHCoAllocString(_pszItemID, ppszItemID);
    } 

    return hr;
}

```