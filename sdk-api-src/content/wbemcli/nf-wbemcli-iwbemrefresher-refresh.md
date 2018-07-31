---
UID: NF:wbemcli.IWbemRefresher.Refresh
title: IWbemRefresher::Refresh
author: windows-sdk-content
description: The IWbemRefresher::Refresh method updates all refreshable objects, enumerators, and nested refreshers. The WMI Refresher calls this function in response to a client request to Refresh.
old-location: wmi\iwbemrefresher_refresh.htm
old-project: WmiSdk
ms.assetid: 6de85040-c938-41dc-8240-0e21e89c7716
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWbemRefresher interface [Windows Management Instrumentation],Refresh method, IWbemRefresher.Refresh, IWbemRefresher::Refresh, Refresh, Refresh method [Windows Management Instrumentation], Refresh method [Windows Management Instrumentation],IWbemRefresher interface, _hmm_iwbemrefresher_refresh, wbemcli/IWbemRefresher::Refresh, wmi.iwbemrefresher_refresh
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemRefresher.Refresh
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

