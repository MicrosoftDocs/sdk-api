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

# ISyncMgrSyncItem::GetItemID


## -description


Gets the unique ID of a sync item.


## -parameters




### -param ppszItemID [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the item's ID. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ID retrieved by this method cannot change. Typically, the ID is in the form of a GUID string. However, this is not a requirement. The ID can be any string that is unique in the context of the handler.

If <b>GetItemID</b> fails or an empty string is returned in <i>ppszItemID</i>, the sync item is not shown in the handler's folder and Sync Center will not attempt to synchronize it.

The ID retrieved by this method is available in the folder UI as the System.Sync.ItemID (PKEY_Sync_HandlerID) property.

The item is responsible for allocating the string buffer pointed to by <i>ppszComment</i> through <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.

In older Sync Manager implementations, this data was retrieved through the <a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a> structure.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::GetItemID(__out LPWSTR *ppszItemID)
{
    HRESULT hr = S_OK;
    *ppszName = NULL;

    // Generate the string version of the ID.
    if (_pszItemID == NULL)
    {
        LPOLESTR pszItemID = NULL;
        hr = StringFromCLSID(_guidItemID, &amp;_pszItemID);
    }

    if (SUCCEEDED(hr))
    {
        // Duplicate the item ID string for the caller.
        hr = SHCoAllocString(_pszItemID, ppszItemID);
    } 

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


