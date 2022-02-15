---
UID: NF:syncmgr.ISyncMgrSyncItem.GetItemInfo
title: ISyncMgrSyncItem::GetItemInfo (syncmgr.h)
description: Gets the properties of a sync item.
helpviewer_keywords: ["GetItemInfo","GetItemInfo method [Windows Shell]","GetItemInfo method [Windows Shell]","ISyncMgrSyncItem interface","ISyncMgrSyncItem interface [Windows Shell]","GetItemInfo method","ISyncMgrSyncItem.GetItemInfo","ISyncMgrSyncItem::GetItemInfo","_shell_ISyncMgrSyncItem_GetItemInfo","shell.ISyncMgrSyncItem_GetItemInfo","syncmgr/ISyncMgrSyncItem::GetItemInfo"]
old-location: shell\ISyncMgrSyncItem_GetItemInfo.htm
tech.root: shell
ms.assetid: b6257d66-36c8-41d6-88f0-99417755582b
ms.date: 12/05/2018
ms.keywords: GetItemInfo, GetItemInfo method [Windows Shell], GetItemInfo method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetItemInfo method, ISyncMgrSyncItem.GetItemInfo, ISyncMgrSyncItem::GetItemInfo, _shell_ISyncMgrSyncItem_GetItemInfo, shell.ISyncMgrSyncItem_GetItemInfo, syncmgr/ISyncMgrSyncItem::GetItemInfo
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
 - ISyncMgrSyncItem::GetItemInfo
 - syncmgr/ISyncMgrSyncItem::GetItemInfo
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
 - ISyncMgrSyncItem.GetItemInfo
---

# ISyncMgrSyncItem::GetItemInfo


## -description

Gets the properties of a sync item.

## -parameters

### -param ppItemInfo [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsynciteminfo">ISyncMgrSyncItemInfo</a>*</b>

When this method returns, contains the address of a pointer to an instance of the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrsynciteminfo">ISyncMgrSyncItemInfo</a> interface, representing the item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <b>GetItemInfo</b> fails, the sync item is still shown in the handler's folder and Sync Center continues to synchronize it, but default values are used for all properties.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceSyncItem::GetItemInfo(
                              __out ISyncMgrSyncItemInfo **ppItemInfo)
{
    *ppItemInfo = NULL;
    
    HRESULT hr = QueryInterface(IID_ISyncMgrSyncItemInfo, (void**)ppItemInfo);
    return hr;
}

```