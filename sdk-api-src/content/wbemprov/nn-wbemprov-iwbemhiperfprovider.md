---
UID: NN:wbemprov.IWbemHiPerfProvider
title: IWbemHiPerfProvider
author: windows-driver-content
description: Enables providers to supply refreshable objects and enumerators.
old-location: wmi\iwbemhiperfprovider.htm
old-project: WmiSdk
ms.assetid: eb0d12c0-d746-4bae-b47d-50350d33447a
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: IWbemHiPerfProvider, IWbemHiPerfProvider interface [Windows Management Instrumentation], IWbemHiPerfProvider interface [Windows Management Instrumentation], described, _hmm_iwbemhiperfprovider, wbemprov/IWbemHiPerfProvider, wmi.iwbemhiperfprovider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wbemprov.h
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
req.typenames: WbemTimeout
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmiprvsd.dll
api_name:
-	IWbemHiPerfProvider
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfProvider interface


## -description


The 
<b>IWbemHiPerfProvider</b> interface enables providers to supply refreshable objects and enumerators. High-performance providers can be loaded in-process to either WMI or a client process. When the provider is loaded in-process to a client process, it uses the CLSID specified as the <b>ClientLoadableCLSID</b> value in the <a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a>  representing the provider instance definition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemHiPerfProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemHiPerfProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemHiPerfProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/086a1717-b6e8-45c1-9397-ec894ee900a0">CreateRefreshableEnum</a>
</td>
<td align="left" width="63%">
Creates a refreshable enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1eb414e0-cdf6-4caa-88a5-8da17a32449c">CreateRefreshableObject</a>
</td>
<td align="left" width="63%">
Creates a refreshable instance object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5962f5f6-a121-4234-8dcd-24c0e2b53990">CreateRefresher</a>
</td>
<td align="left" width="63%">
Creates a refresher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba56b029-95d4-4c79-8385-0a5adb9f7dcc">GetObjects</a>
</td>
<td align="left" width="63%">
Retrieves the specified objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8962fe9d-4b3e-469b-83e7-9c3f62a24308">QueryInstances</a>
</td>
<td align="left" width="63%">
Returns instances of the specified class by using the supplied 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1de54de-b57b-4e15-84b3-96cc36bf023b">StopRefreshing</a>
</td>
<td align="left" width="63%">
Stops refreshing an enumerator or instance object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/2158385f-d0dc-4102-84db-ce02d2b0ee53">Accessing WMI Preinstalled Performance Classes</a>



<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/a4f537ba-9081-43b4-acff-4d206de3d9d7">Developing a WMI Provider</a>



<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a>



Making an Instance Provider into a High-Performance Provider



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Writing an Instance Provider</a>
 

 

