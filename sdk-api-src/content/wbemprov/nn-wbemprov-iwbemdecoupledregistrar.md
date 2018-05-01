---
UID: NN:wbemprov.IWbemDecoupledRegistrar
title: IWbemDecoupledRegistrar
author: windows-driver-content
description: The IWbemDecoupledRegistrar interface associates decoupled providers with WMI. This interface allows a process-hosted provider to define the interoperability lifetime of the interface and to coexist with other providers.
old-location: wmi\iwbemdecoupledregistrar.htm
old-project: WmiSdk
ms.assetid: ec805089-aff4-4885-b650-a784ce25a7d3
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWbemDecoupledRegistrar, IWbemDecoupledRegistrar interface [Windows Management Instrumentation], IWbemDecoupledRegistrar interface [Windows Management Instrumentation], described, _hmm_iwbemdecoupledregistrar, wbemprov/IWbemDecoupledRegistrar, wmi.iwbemdecoupledregistrar
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
req.idl: Wbemprov.idl
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
-	Wmidcprv.dll
api_name:
-	IWbemDecoupledRegistrar
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmidcprv.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemDecoupledRegistrar interface


## -description


The 
<b>IWbemDecoupledRegistrar</b> interface associates decoupled providers with WMI. This interface allows a process-hosted provider to define the interoperability lifetime of the interface and to coexist with other providers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemDecoupledRegistrar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemDecoupledRegistrar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemDecoupledRegistrar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0592310c-dc1b-45df-bf60-613a58dd69ad">Register</a>
</td>
<td align="left" width="63%">
Registers an object interface with WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24e9cc0c-20c4-464b-a215-4d0344bc4565">UnRegister</a>
</td>
<td align="left" width="63%">
Removes an object interface from registration with WMI.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/a502f0dd-9add-4ebd-bc25-743a55eb78ac">Incorporating a Provider in an Application</a>
 

 

