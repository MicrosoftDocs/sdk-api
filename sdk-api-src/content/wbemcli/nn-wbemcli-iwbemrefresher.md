---
UID: NN:wbemcli.IWbemRefresher
title: IWbemRefresher (wbemcli.h)
description: Provides an entry point through which refreshable objects such as enumerators or refresher objects, can be refreshed.
helpviewer_keywords: ["IWbemRefresher","IWbemRefresher interface [Windows Management Instrumentation]","IWbemRefresher interface [Windows Management Instrumentation]","described","WbemRefresher","_hmm_iwbemrefresher","wbemcli/IWbemRefresher","wmi.iwbemrefresher"]
old-location: wmi\iwbemrefresher.htm
tech.root: WmiSdk
ms.assetid: cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed
ms.date: 12/05/2018
ms.keywords: IWbemRefresher, IWbemRefresher interface [Windows Management Instrumentation], IWbemRefresher interface [Windows Management Instrumentation],described, WbemRefresher, _hmm_iwbemrefresher, wbemcli/IWbemRefresher, wmi.iwbemrefresher
f1_keywords:
- wbemcli/IWbemRefresher
dev_langs:
- c++
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
- IWbemRefresher
- WbemRefresher
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemRefresher interface


## -description


The 
<b>IWbemRefresher</b> interface provides an entry point through which refreshable objects such as enumerators or refresher objects, can be refreshed. Implementers of 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a> must provide an implementation of this interface.

WMI supplies a client implementation of this interface. Clients can access this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> on <b>CLSID_WbemRefresher</b>. This is the only supported implementation on the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemRefresher</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemRefresher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemRefresher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Updates information in this refresher.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/writing-an-instance-provider">Writing an Instance Provider</a>
 

 

