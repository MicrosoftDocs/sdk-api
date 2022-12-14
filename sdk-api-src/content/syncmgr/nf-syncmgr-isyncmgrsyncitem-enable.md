---
UID: NF:syncmgr.ISyncMgrSyncItem.Enable
title: ISyncMgrSyncItem::Enable (syncmgr.h)
description: Enables or disables the sync item.
helpviewer_keywords: ["Enable","Enable method [Windows Shell]","Enable method [Windows Shell]","ISyncMgrSyncItem interface","ISyncMgrSyncItem interface [Windows Shell]","Enable method","ISyncMgrSyncItem.Enable","ISyncMgrSyncItem::Enable","_shell_ISyncMgrSyncItem_Enable","shell.ISyncMgrSyncItem_Enable","syncmgr/ISyncMgrSyncItem::Enable"]
old-location: shell\ISyncMgrSyncItem_Enable.htm
tech.root: shell
ms.assetid: 7d73508e-4381-47fe-98ba-ab3ef665cd3e
ms.date: 12/05/2018
ms.keywords: Enable, Enable method [Windows Shell], Enable method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],Enable method, ISyncMgrSyncItem.Enable, ISyncMgrSyncItem::Enable, _shell_ISyncMgrSyncItem_Enable, shell.ISyncMgrSyncItem_Enable, syncmgr/ISyncMgrSyncItem::Enable
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
 - ISyncMgrSyncItem::Enable
 - syncmgr/ISyncMgrSyncItem::Enable
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
 - ISyncMgrSyncItem.Enable
---

# ISyncMgrSyncItem::Enable


## -description

Enables or disables the sync item.

## -parameters

### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable; <b>FALSE</b> to disable.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Sync Center calls this method in the following scenarios.
            
                

<ul>
<li>When the user selects the item in the handler's folder and launches its <b>Enable</b> task, but only if the item has not set the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_IPM_PREVENT_ENABLE</a> flag. If the handler supports the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">SYNCMGR_OBJECTID_QueryBeforeEnable</a> object, this method is only called if the UI operation was successful.</li>
<li>When the user selects the item in the handler's folder and launches its <b>Disable</b> task, but only if the item has not set the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_IPM_PREVENT_DISABLE</a> flag. If the handler supports the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">SYNCMGR_OBJECTID_QueryBeforeDisable</a> object, this method is only called if the UI operation was successful.</li>
</ul>
If the handler does not need to perform any actions when it is activated, it can return either S_OK or E_NOTIMPL as shown in the example below.


#### Examples



The following example shows a simple implementation of this method.


```cpp
STDMETHODIMP CMyDeviceSyncItem::Enable(__in BOOL fEnable)
{
    return E_NOTIMPL;
}

```