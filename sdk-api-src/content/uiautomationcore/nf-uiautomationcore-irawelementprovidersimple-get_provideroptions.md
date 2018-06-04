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

# IRawElementProviderSimple::get_ProviderOptions


## -description


Specifies the type of Microsoft UI Automation provider; for example, whether it is a client-side (proxy) or server-side provider.

This property is read-only.


## -parameters


## -remarks



The method must return either <a href="uiauto_ProvOptionsEnum.htm">ProviderOptions_ServerSideProvider</a> or <a href="uiauto_ProvOptionsEnum.htm">ProviderOptions_ClientSideProvider</a>.

UI Automation handles the various types of providers differently. 
			For example, events from a server-side provider are broadcast to all listening clients, 
			but events from client-side (proxy) providers remain in the client.


#### Examples

The following example implements this method for a server-side UI Automation provider.
			

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT STDMETHODCALLTYPE Provider::get_ProviderOptions( ProviderOptions* pRetVal )
{
    *pRetVal = ProviderOptions_ServerSideProvider;
    return S_OK;
}    </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>
 

 

