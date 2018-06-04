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

# IWbemRefresher::Refresh


## -description


The 
<b>IWbemRefresher::Refresh</b> method updates all refreshable objects, enumerators, and nested refreshers. The WMI Refresher calls this function in response to a client request to 
<b>Refresh</b>.


## -parameters




### -param lFlags [in]

Bitmask of flags that modify the behavior of this method.

If <b>WBEM_FLAG_REFRESH_AUTO_RECONNECT</b> is specified and if the connection is broken, the refresher attempts to reconnect to the provider automatically. This is the default behavior for this method.

If you do not want the refresher to attempt to reconnect to the provider, specify <b>WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT</b>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



When refreshing enumerators and objects, providers should take as little time as possible. Using the 
<a href="https://msdn.microsoft.com/1025ae50-870f-4d38-8e83-3c6b628315c6">IWbemObjectAccess</a> methods and caching property handles for reuse can dramatically improve performance. When updating enumerators, a provider can either remove and re-instantiate all objects, or simply remove and add the changed instances. It is up to you to choose the best approach. In either case, caching instances can improve performance.

The provider should only access the objects and enumerators in a refresher in response to a call to 
<b>IWbemRefresher::Refresh</b>. It would, however, be perfectly valid to have a background thread polling for data with which to fill these objects, to prepare for when 
<b>Refresh</b> is called.


#### Examples

The following code example describes how to implement 
<b>Refresh</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CMyHiPerfProviderRefresher::Refresh(
/* [in] */long lFlags
)
{
  // Run through all the objects and update their
  // data.

  // Now run through the enumerators.
  // Empty the enumerator and refill it.
   

  return WBEM_S_NO_ERROR;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a4f537ba-9081-43b4-acff-4d206de3d9d7">Developing a WMI Provider</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a>



Making an Instance Provider into a High-Performance Provider



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Writing an Instance Provider</a>
 

 

