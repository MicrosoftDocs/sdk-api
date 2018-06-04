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

# ISyncMgrSyncItem::GetItemInfo


## -description


Gets the properties of a sync item.


## -parameters




### -param ppItemInfo [out]

Type: <b><a href="https://msdn.microsoft.com/b98d216e-f23f-45f3-b42d-e5aa2e540265">ISyncMgrSyncItemInfo</a>*</b>

When this method returns, contains the address of a pointer to an instance of the <a href="https://msdn.microsoft.com/b98d216e-f23f-45f3-b42d-e5aa2e540265">ISyncMgrSyncItemInfo</a> interface, representing the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <b>GetItemInfo</b> fails, the sync item is still shown in the handler's folder and Sync Center continues to synchronize it, but default values are used for all properties.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::GetItemInfo(
                              __out ISyncMgrSyncItemInfo **ppItemInfo)
{
    *ppItemInfo = NULL;
    
    HRESULT hr = QueryInterface(IID_ISyncMgrSyncItemInfo, (void**)ppItemInfo);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


