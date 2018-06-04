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

# ISyncMgrSyncItemContainer::GetSyncItemEnumerator


## -description


Gets an interface that enumerates the handler's sync items.


## -parameters




### -param ppenum [out]

Type: <b><a href="https://msdn.microsoft.com/0d1695e2-6936-4f53-9594-e0e2bc69afd4">IEnumSyncMgrSyncItems</a>**</b>

When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/0d1695e2-6936-4f53-9594-e0e2bc69afd4">IEnumSyncMgrSyncItems</a> instance. <b>IEnumSyncMgrSyncItems</b> can be used to retrieve an interface for each sync item in the set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method replaces the older <a href="https://msdn.microsoft.com/75f6ce68-237f-4228-adcf-f5ec929f49a7">EnumSyncMgrItems</a> method. The older method returned an enumerator interface which returned a <a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a> structure for each sync item. To get the data previously provided by that structure, Sync Center calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on each item's <a href="https://msdn.microsoft.com/322c2ebe-f1ab-4de4-b8d5-2fba1e69ddda">ISyncMgrSyncItem</a> interface to request a corresponding <a href="https://msdn.microsoft.com/b98d216e-f23f-45f3-b42d-e5aa2e540265">ISyncMgrSyncItemInfo</a> interface.

The number of enumerated items can be obtained through the <a href="https://msdn.microsoft.com/bbe37dff-d758-41ca-872d-4607d605011d">ISyncMgrSyncItemContainer::GetSyncItemCount</a> method.


#### Examples

The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetSyncItemEnumerator(
    __out IEnumSyncMgrSyncItems **ppenum)
{
    *ppenum = NULL;

    // Load the items using a private class method.
    HRESULT hr = _LoadItems();

    if (SUCCEEDED(hr))
    {
        hr = CEnumSyncMgrSyncItems_CreateInstance(this,
                                                  IID_PPV_ARGS(ppenum));
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


