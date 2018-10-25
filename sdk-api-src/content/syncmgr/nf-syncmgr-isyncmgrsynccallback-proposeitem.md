---
UID: NF:syncmgr.ISyncMgrSyncCallback.ProposeItem
title: ISyncMgrSyncCallback::ProposeItem
author: windows-sdk-content
description: Proposes the addition of a new item to the set of items previously enumerated.
old-location: shell\ISyncMgrSyncCallback_ProposeItem.htm
tech.root: shell
ms.assetid: d0c73950-f80e-4831-9c56-4316561a269b
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ISyncMgrSyncCallback interface [Windows Shell],ProposeItem method, ISyncMgrSyncCallback.ProposeItem, ISyncMgrSyncCallback::ProposeItem, ProposeItem, ProposeItem method [Windows Shell], ProposeItem method [Windows Shell],ISyncMgrSyncCallback interface, _shell_ISyncMgrSyncCallback_ProposeItem, shell.ISyncMgrSyncCallback_ProposeItem, syncmgr/ISyncMgrSyncCallback::ProposeItem
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
 - ISyncMgrSyncCallback.ProposeItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncCallback::ProposeItem


## -description


Proposes the addition of a new item to the set of items previously enumerated.


## -parameters




### -param pNewItem [in]

Type: <b><a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a>*</b>

A pointer to an instance of <a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a> representing the new item.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns E_INVALIDARG if <i>pszItemID</i> already exists.




## -remarks



<b>ISyncMgrSyncCallback::ProposeItem</b> is typically called when items are not considered part of the sync set unless they have been successfully synchronized. Sync Center does not display this item in the UI until the <a href="https://msdn.microsoft.com/e0964cd3-42ad-4af0-90b2-0f365f457448">ISyncMgrSyncCallback::CommitItem</a> method has been called.


#### Examples



The following example shows the usage of <b>ISyncMgrSyncCallback::ProposeItem</b> and <a href="https://msdn.microsoft.com/e0964cd3-42ad-4af0-90b2-0f365f457448">ISyncMgrSyncCallback::CommitItem</a> by the <a href="https://msdn.microsoft.com/6742f6a8-eda8-4ef0-8a11-dc70baefcc83">Synchronize</a> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CMyDeviceHandler::Synchronize(...)
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
        
        hr = GetNextNewItem(&amp;pNewItem, szItemID, ARRAYSIZE(szItemID));
        if (SUCCEEDED(hr))
        {
            // Propose this item to Sync Center.
            hr = pCallback-&gt;ProposeItem(pNewItem);
            if (SUCCEEDED(hr))
            {
                // Synchronize the item.
                // Synchronization was successful.  Commit the item.
                hr = pCallback-&gt;CommitItem(szItemID);
            }
            pNewItem-&gt;Release();
        }
    }
    ...
}
</pre>
</td>
</tr>
</table></span></div>


