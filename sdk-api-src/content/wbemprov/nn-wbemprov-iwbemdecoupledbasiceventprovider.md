---
UID: NN:wbemprov.IWbemDecoupledBasicEventProvider
title: IWbemDecoupledBasicEventProvider (wbemprov.h)
author: windows-sdk-content
description: The IWbemDecoupledBasicEventProvider interface is a cocreatable interface that registers decoupled providers with WMI. The object created should be passed into the pUnknown argument of IWbemDecoupledRegistrar::Register.
old-location: wmi\iwbemdecoupledbasiceventprovider.htm
tech.root: WmiSdk
ms.assetid: 71ce4f79-8168-47c5-a8b1-4286b34f7a31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWbemDecoupledBasicEventProvider, IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation], IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation],described, _hmm_iwbemdecoupledbasiceventprovider, wbemprov/IWbemDecoupledBasicEventProvider, wmi.iwbemdecoupledbasiceventprovider
ms.topic: interface
f1_keywords: 
 - "wbemprov/IWbemDecoupledBasicEventProvider"
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
req.idl: Wbemprov.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmidcprv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmidcprv.dll
api_name:
 - IWbemDecoupledBasicEventProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemDecoupledBasicEventProvider interface


## -description


The 
<b>IWbemDecoupledBasicEventProvider</b> interface is a cocreatable interface that  registers decoupled providers with WMI. The object created should be passed into the <i>pUnknown </i>argument of 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register">IWbemDecoupledRegistrar::Register</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemDecoupledBasicEventProvider</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nn-wbemprov-iwbemdecoupledregistrar">IWbemDecoupledRegistrar</a>. <b>IWbemDecoupledBasicEventProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemDecoupledBasicEventProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledbasiceventprovider-getservice">GetService</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> object for calling back to WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledbasiceventprovider-getsink">GetSink</a>
</td>
<td align="left" width="63%">
Creates an object sink for event forwarding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa391480(v=vs.85)">Register</a>
</td>
<td align="left" width="63%">
Registers an object interface with WMI.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nn-wbemprov-iwbemdecoupledregistrar">IWbemDecoupledRegistrar</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application">Incorporating a Provider in an Application</a>
 

 

