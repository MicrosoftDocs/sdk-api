---
UID: NF:syncmgr.ISyncMgrSyncItem.GetPolicies
title: ISyncMgrSyncItem::GetPolicies (syncmgr.h)
description: Gets a set of flags describing the policies set by the item.
helpviewer_keywords: ["GetPolicies","GetPolicies method [Windows Shell]","GetPolicies method [Windows Shell]","ISyncMgrSyncItem interface","ISyncMgrSyncItem interface [Windows Shell]","GetPolicies method","ISyncMgrSyncItem.GetPolicies","ISyncMgrSyncItem::GetPolicies","_shell_ISyncMgrSyncItem_GetPolicies","shell.ISyncMgrSyncItem_GetPolicies","syncmgr/ISyncMgrSyncItem::GetPolicies"]
old-location: shell\ISyncMgrSyncItem_GetPolicies.htm
tech.root: shell
ms.assetid: 5f4e1a8e-8fa7-48b3-8f20-8b260540ab9c
ms.date: 12/05/2018
ms.keywords: GetPolicies, GetPolicies method [Windows Shell], GetPolicies method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetPolicies method, ISyncMgrSyncItem.GetPolicies, ISyncMgrSyncItem::GetPolicies, _shell_ISyncMgrSyncItem_GetPolicies, shell.ISyncMgrSyncItem_GetPolicies, syncmgr/ISyncMgrSyncItem::GetPolicies
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
 - ISyncMgrSyncItem::GetPolicies
 - syncmgr/ISyncMgrSyncItem::GetPolicies
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
 - ISyncMgrSyncItem.GetPolicies
---

# ISyncMgrSyncItem::GetPolicies


## -description

Gets a set of flags describing the policies set by the item.

## -parameters

### -param pmPolicies [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_policies">SYNCMGR_ITEM_POLICIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_policies">SYNCMGR_ITEM_POLICIES</a> enumeration that defines the item's policies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A policy is an action that is typically supported but can be disabled by a group policy.

This method is called by Sync Center in response to a call to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updateitem">UpdateItem</a>.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceSyncItem::GetPolicies(
                              __out SYNCMGR_ITEM_POLICIES *pmPolicies)
{
    *pmPolicies = SYNCMGR_IPM_PREVENT_DISABLE 
                | SYNCMGR_IPM_HIDDEN_BY_DEFAULT;
                
    return S_OK;
}

```