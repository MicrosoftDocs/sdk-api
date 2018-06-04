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

# ISyncMgrEventStore::GetEventEnumerator


## -description


Gets an enumerator for a handler's events.


## -parameters




### -param ppenum [out]

Type: <b><a href="https://msdn.microsoft.com/74d0c373-e9b1-4d9c-bdb6-caa743938e32">IEnumSyncMgrEvents</a>**</b>

When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/74d0c373-e9b1-4d9c-bdb6-caa743938e32">IEnumSyncMgrEvents</a> instance that can be used to access the handler's events.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by Sync Center when the user navigates to the Sync Results folder or clicks the <b>Errors</b> link for a handler.


#### Examples




        	The following example shows an implementation of <b>ISyncMgrEventStore::GetEventEnumerator</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceEventStore::GetEventEnumerator(
                                __out IEnumSyncMgrEvents **ppenum)
{
    HRESULT hr = CEnumMyDeviceSyncMgrEvents_Create(ppenum);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


