---
UID: NN:wbemcli.IWbemConfigureRefresher
title: IWbemConfigureRefresher (wbemcli.h)
author: windows-sdk-content
description: The IWbemConfigureRefresher interface is used by client code to add enumerators, objects, and nested refreshers into a refresher.
old-location: wmi\iwbemconfigurerefresher.htm
tech.root: WmiSdk
ms.assetid: 9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWbemConfigureRefresher, IWbemConfigureRefresher interface [Windows Management Instrumentation], IWbemConfigureRefresher interface [Windows Management Instrumentation],described, _hmm_iwbemconfigurerefresher, wbemcli/IWbemConfigureRefresher, wmi.iwbemconfigurerefresher
ms.topic: interface
f1_keywords: 
 - "wbemcli/IWbemConfigureRefresher"
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
req.lib: Wbemuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemConfigureRefresher
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemConfigureRefresher interface


## -description


The 
<b>IWbemConfigureRefresher</b> interface is used by client code to add enumerators, objects, and nested refreshers into a refresher.

Users and providers should never implement this interface. The implementation provided by WMI is the only one that is supported.

By providing a native implementation of this interface, WMI allows client code to easily configure refreshers. You can access the 
<b>IWbemConfigureRefresher</b> interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on <b>IID_IWbemConfigureRefresher</b> on the object returned by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> on <b>CLSID_WbemRefresher</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemConfigureRefresher</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemConfigureRefresher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemConfigureRefresher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum">AddEnum</a>
</td>
<td align="left" width="63%">
Adds an enumerator to a refresher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath">AddObjectByPath</a>
</td>
<td align="left" width="63%">
Adds an object to a refresher based on a relative path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbytemplate">AddObjectByTemplate</a>
</td>
<td align="left" width="63%">
Adds an object to a refresher by specifying an 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> instance template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addrefresher">AddRefresher</a>
</td>
<td align="left" width="63%">
Adds a refresher to a refresher.

Use this method to create a single refresher that contains more than one refresher, which can be updated using a single call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">Refresh</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an object, enumerator, or nested refresher from a refresher.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>
 

 

