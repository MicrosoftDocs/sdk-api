---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

    // Check for additional items to sync.
    IEnumString *penumItemIDs = NULL;
    
    hr = pCallback-&gt;QueryForAdditionalItems(&amp;penumItemIDs);
    if (hr == S_OK)
    {
        while (hr == S_OK)
        {
            LPWSTR pszItemID;
            ULONG cFetched;
            hr = penumItemIDs-&gt;Next(1, &amp;pszItemID, &amp;cFetched);
            if ((hr == S_OK) &amp;&amp; (cFetched == 1))
            {
                // Add this item to the set of items we are syncing.
                hr = pCallback-&gt;AddItemToSession(pszItemID);
                CoTaskMemFree(pszItemID);
            }
        }
        penumItemIDs-&gt;Release();
    }
    ...
}
</pre>
</td>
</tr>
</table></span></div>


