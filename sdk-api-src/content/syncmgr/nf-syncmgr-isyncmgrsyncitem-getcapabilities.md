---
UID: NF:syncmgr.ISyncMgrSyncItem.GetCapabilities
title: ISyncMgrSyncItem::GetCapabilities
author: windows-sdk-content
description: Gets a set of flags describing the item's defined capabilities.
old-location: shell\ISyncMgrSyncItem_GetCapabilities.htm
tech.root: shell
ms.assetid: 6cb98b83-cf17-451c-ba29-700408f474c7
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetCapabilities, GetCapabilities method [Windows Shell], GetCapabilities method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetCapabilities method, ISyncMgrSyncItem.GetCapabilities, ISyncMgrSyncItem::GetCapabilities, _shell_ISyncMgrSyncItem_GetCapabilities, shell.ISyncMgrSyncItem_GetCapabilities, syncmgr/ISyncMgrSyncItem::GetCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncItem.GetCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncItem::GetCapabilities


## -description


Gets a set of flags describing the item's defined capabilities.


## -parameters




### -param pmCapabilities [out]

Type: <b><a href="https://msdn.microsoft.com/55f72e18-fba6-4a59-b553-06c6c7c3ee52">SYNCMGR_ITEM_CAPABILITIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="https://msdn.microsoft.com/55f72e18-fba6-4a59-b553-06c6c7c3ee52">SYNCMGR_ITEM_CAPABILITIES</a> enumeration that defines the capabilities of the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by Sync Center in response to a call to <a href="https://msdn.microsoft.com/deb87d2f-74da-450a-a424-505240eadacb">UpdateItem</a>.


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




