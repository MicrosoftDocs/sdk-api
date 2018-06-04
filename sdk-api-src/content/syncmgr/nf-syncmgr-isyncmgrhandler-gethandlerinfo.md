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

# ISyncMgrHandler::GetHandlerInfo


## -description


Gets properties that describe the handler.


## -parameters




### -param ppHandlerInfo [out]

Type: <b><a href="https://msdn.microsoft.com/29cded59-d0f3-4678-9601-4931687b48e4">ISyncMgrHandlerInfo</a>**</b>

When this method returns, contains the address of a pointer to an instance of the <a href="https://msdn.microsoft.com/29cded59-d0f3-4678-9601-4931687b48e4">ISyncMgrHandlerInfo</a> interface that provides access to the handler properties.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method fails, the handler is still shown in the Sync Center folder and Sync Center continues to invoke it, but default values are used for all properties.

<b>ISyncMgrHandler::GetHandlerInfo</b>, together with <a href="https://msdn.microsoft.com/2d981cf9-6c0a-4bca-b088-06eb1c820fb3">ISyncMgrHandler::GetName</a>, replaces the older <a href="https://msdn.microsoft.com/bae3ead8-632c-45bf-a24e-bf07922039bd">GetHandlerInfo</a>.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetHandlerInfo(
                             __out ISyncMgrHandlerInfo **ppHandlerInfo)
{
    *ppHandlerInfo = NULL;
    HRESULT hr = QueryInterface(IID_ISyncMgrHandlerInfo, 
                                (void **) ppHandlerInfo);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


