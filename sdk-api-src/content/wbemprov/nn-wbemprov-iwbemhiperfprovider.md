---
UID: NN:wbemprov.IWbemHiPerfProvider
title: IWbemHiPerfProvider (wbemprov.h)

description: Enables providers to supply refreshable objects and enumerators.
old-location: wmi\iwbemhiperfprovider.htm
tech.root: WmiSdk
ms.assetid: eb0d12c0-d746-4bae-b47d-50350d33447a

ms.date: 12/05/2018
ms.keywords: IWbemHiPerfProvider, IWbemHiPerfProvider interface [Windows Management Instrumentation], IWbemHiPerfProvider interface [Windows Management Instrumentation],described, _hmm_iwbemhiperfprovider, wbemprov/IWbemHiPerfProvider, wmi.iwbemhiperfprovider
ms.topic: interface
f1_keywords: 
 - "wbemprov/IWbemHiPerfProvider"
dev_langs:
 - c++
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
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiprvsd.dll
api_name:
 - IWbemHiPerfProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemHiPerfProvider interface


## -description


The 
<b>IWbemHiPerfProvider</b> interface enables providers to supply refreshable objects and enumerators. High-performance providers can be loaded in-process to either WMI or a client process. When the provider is loaded in-process to a client process, it uses the CLSID specified as the <b>ClientLoadableCLSID</b> value in the <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/--win32provider">__Win32Provider</a>  representing the provider instance definition.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemHiPerfProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemHiPerfProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum">CreateRefreshableEnum</a>
</td>
<td align="left" width="63%">
Creates a refreshable enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject">CreateRefreshableObject</a>
</td>
<td align="left" width="63%">
Creates a refreshable instance object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher">CreateRefresher</a>
</td>
<td align="left" width="63%">
Creates a refresher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects">GetObjects</a>
</td>
<td align="left" width="63%">
Retrieves the specified objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances">QueryInstances</a>
</td>
<td align="left" width="63%">
Returns instances of the specified class by using the supplied 
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing">StopRefreshing</a>
</td>
<td align="left" width="63%">
Stops refreshing an enumerator or instance object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-wmi-preinstalled-performance-classes">Accessing WMI Preinstalled Performance Classes</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a>



Making an Instance Provider into a High-Performance Provider



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>
 

 

