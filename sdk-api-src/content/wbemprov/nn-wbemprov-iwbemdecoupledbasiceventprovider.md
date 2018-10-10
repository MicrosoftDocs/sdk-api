---
UID: NN:wbemprov.IWbemDecoupledBasicEventProvider
title: IWbemDecoupledBasicEventProvider
author: windows-sdk-content
description: The IWbemDecoupledBasicEventProvider interface is a cocreatable interface that registers decoupled providers with WMI. The object created should be passed into the pUnknown argument of IWbemDecoupledRegistrar::Register.
old-location: wmi\iwbemdecoupledbasiceventprovider.htm
tech.root: WmiSdk
ms.assetid: 71ce4f79-8168-47c5-a8b1-4286b34f7a31
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IWbemDecoupledBasicEventProvider, IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation], IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation],described, _hmm_iwbemdecoupledbasiceventprovider, wbemprov/IWbemDecoupledBasicEventProvider, wmi.iwbemdecoupledbasiceventprovider
ms.prod: windows
ms.technology: windows-sdk
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemDecoupledBasicEventProvider interface


## -description


The 
<b>IWbemDecoupledBasicEventProvider</b> interface is a cocreatable interface that  registers decoupled providers with WMI. The object created should be passed into the <i>pUnknown </i>argument of 
<a href="https://msdn.microsoft.com/0592310c-dc1b-45df-bf60-613a58dd69ad">IWbemDecoupledRegistrar::Register</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemDecoupledBasicEventProvider</b> interface inherits from <a href="https://msdn.microsoft.com/ec805089-aff4-4885-b650-a784ce25a7d3">IWbemDecoupledRegistrar</a>. <b>IWbemDecoupledBasicEventProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d9ce6d1b-4e4a-4d36-8957-85471fff3c69">GetService</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> object for calling back to WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b33e441-4bc4-47ed-b09b-7af859127b06">GetSink</a>
</td>
<td align="left" width="63%">
Creates an object sink for event forwarding.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecae214b-e474-42db-b489-fec99b6aeefc">Register</a>
</td>
<td align="left" width="63%">
Registers an object interface with WMI.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/ec805089-aff4-4885-b650-a784ce25a7d3">IWbemDecoupledRegistrar</a>



<a href="https://msdn.microsoft.com/a502f0dd-9add-4ebd-bc25-743a55eb78ac">Incorporating a Provider in an Application</a>
 

 

