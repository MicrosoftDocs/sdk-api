---
UID: NF:syncmgr.ISyncMgrSyncItem.GetCapabilities
title: ISyncMgrSyncItem::GetCapabilities (syncmgr.h)
description: Gets a set of flags describing the item's defined capabilities.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [Windows Shell]","GetCapabilities method [Windows Shell]","ISyncMgrSyncItem interface","ISyncMgrSyncItem interface [Windows Shell]","GetCapabilities method","ISyncMgrSyncItem.GetCapabilities","ISyncMgrSyncItem::GetCapabilities","_shell_ISyncMgrSyncItem_GetCapabilities","shell.ISyncMgrSyncItem_GetCapabilities","syncmgr/ISyncMgrSyncItem::GetCapabilities"]
old-location: shell\ISyncMgrSyncItem_GetCapabilities.htm
tech.root: shell
ms.assetid: 6cb98b83-cf17-451c-ba29-700408f474c7
ms.date: 12/05/2018
ms.keywords: GetCapabilities, GetCapabilities method [Windows Shell], GetCapabilities method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetCapabilities method, ISyncMgrSyncItem.GetCapabilities, ISyncMgrSyncItem::GetCapabilities, _shell_ISyncMgrSyncItem_GetCapabilities, shell.ISyncMgrSyncItem_GetCapabilities, syncmgr/ISyncMgrSyncItem::GetCapabilities
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
 - ISyncMgrSyncItem::GetCapabilities
 - syncmgr/ISyncMgrSyncItem::GetCapabilities
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
 - ISyncMgrSyncItem.GetCapabilities
---

# ISyncMgrSyncItem::GetCapabilities


## -description

Gets a set of flags describing the item's defined capabilities.

## -parameters

### -param pmCapabilities [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ITEM_CAPABILITIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ITEM_CAPABILITIES</a> enumeration that defines the capabilities of the item.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by Sync Center in response to a call to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateitem">UpdateItem</a>.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceSyncItem::GetCapabilities(
                              __out SYNCMGR_ITEM_CAPABILITIES *pmCapabilities)
{
    *pmCapabilities = SYNCMGR_ICM_EVENT_STORE
                    | SYNCMGR_ICM_CAN_DELETE
                    | SYNCMGR_ICM_QUERY_BEFORE_DELETE;
    
    return S_OK;
}

```