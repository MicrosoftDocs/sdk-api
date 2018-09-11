---
UID: NF:syncmgr.ISyncMgrSyncCallback.AddItemToSession
title: ISyncMgrSyncCallback::AddItemToSession
author: windows-sdk-content
description: Adds a specified item to the set of items currently being synchronized.
old-location: shell\ISyncMgrSyncCallback_AddItemToSession.htm
tech.root: shell
ms.assetid: 1de3d6c0-cdf8-48fa-b7ff-2dc75f6757fc
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: AddItemToSession, AddItemToSession method [Windows Shell], AddItemToSession method [Windows Shell],ISyncMgrSyncCallback interface, ISyncMgrSyncCallback interface [Windows Shell],AddItemToSession method, ISyncMgrSyncCallback.AddItemToSession, ISyncMgrSyncCallback::AddItemToSession, _shell_ISyncMgrSyncCallback_AddItemToSession, shell.ISyncMgrSyncCallback_AddItemToSession, syncmgr/ISyncMgrSyncCallback::AddItemToSession
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
 - ISyncMgrSyncCallback.AddItemToSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncCallback::AddItemToSession


## -description


Adds a specified item to the set of items currently being synchronized.


## -parameters




### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the item to add. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns E_INVALIDARG if <i>pszItemID</i> is already part of the session.




## -remarks



<b>ISyncMgrSyncCallback::AddItemToSession</b> is called by the sync handler.


#### Examples



The following example shows the usage of <b>ISyncMgrSyncCallback::AddItemToSession</b> by the <a href="https://msdn.microsoft.com/6742f6a8-eda8-4ef0-8a11-dc70baefcc83">Synchronize</a> method.


```cpp
HRESULT CMyDeviceHandler::Synchronize(...)
{
    ...

    // Start synchronizing the handler.

    ...

    // Check for additional items to sync.
    IEnumString *penumItemIDs = NULL;
    
    hr = pCallback->QueryForAdditionalItems(&penumItemIDs);
    if (hr == S_OK)
    {
        while (hr == S_OK)
        {
            LPWSTR pszItemID;
            ULONG cFetched;
            hr = penumItemIDs->Next(1, &pszItemID, &cFetched);
            if ((hr == S_OK) && (cFetched == 1))
            {
                // Add this item to the set of items we are syncing.
                hr = pCallback->AddItemToSession(pszItemID);
                CoTaskMemFree(pszItemID);
            }
        }
        penumItemIDs->Release();
    }
    ...
}

```




