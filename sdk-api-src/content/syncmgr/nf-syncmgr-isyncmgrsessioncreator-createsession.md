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

# ISyncMgrSessionCreator::CreateSession


## -description


Notifies Sync Center that synchronization of the specified items has begun.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param ppszItemIDs [in]

Type: <b>LPCWSTR*</b>

The address of a pointer to a buffer containing an array of item IDs, managed by the handler specified in <i>pszHandlerID</i>, to be synchronized. Each ID is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param cItems [in]

Type: <b>ULONG</b>

The number of item IDs contained in the buffer referenced in <i>ppszItemIDs</i>.


### -param ppCallback [in]

Type: <b><a href="https://msdn.microsoft.com/4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397">ISyncMgrSyncCallback</a>**</b>

The address of a pointer to an instance of <a href="https://msdn.microsoft.com/4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397">ISyncMgrSyncCallback</a> used to report progress and events. This value can be <b>NULL</b> if no callback is needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Both <i>pszHandlerID</i> and <i>ppszItemIDs</i> must be specified.


#### Examples




        	The following example shows the outline of an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::Synchronize(...)
{
    ...
    ISyncMgrSyncCallback *pCallback = NULL;

    hr = pCreator-&gt;CreateSession(_pszHandlerID, ppszItemIDs, cItems, &amp;pCallback);
    if (SUCCEEDED(hr))
    {
        // Perform synchronization.
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


