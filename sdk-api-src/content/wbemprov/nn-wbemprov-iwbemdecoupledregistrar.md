---
UID: NN:wbemprov.IWbemDecoupledRegistrar
title: IWbemDecoupledRegistrar (wbemprov.h)
description: The IWbemDecoupledRegistrar interface associates decoupled providers with WMI. This interface allows a process-hosted provider to define the interoperability lifetime of the interface and to coexist with other providers.
helpviewer_keywords: ["IWbemDecoupledRegistrar","IWbemDecoupledRegistrar interface [Windows Management Instrumentation]","IWbemDecoupledRegistrar interface [Windows Management Instrumentation]","described","_hmm_iwbemdecoupledregistrar","wbemprov/IWbemDecoupledRegistrar","wmi.iwbemdecoupledregistrar"]
old-location: wmi\iwbemdecoupledregistrar.htm
tech.root: wmi
ms.assetid: ec805089-aff4-4885-b650-a784ce25a7d3
ms.date: 12/05/2018
ms.keywords: IWbemDecoupledRegistrar, IWbemDecoupledRegistrar interface [Windows Management Instrumentation], IWbemDecoupledRegistrar interface [Windows Management Instrumentation],described, _hmm_iwbemdecoupledregistrar, wbemprov/IWbemDecoupledRegistrar, wmi.iwbemdecoupledregistrar
f1_keywords:
- wbemprov/IWbemDecoupledRegistrar
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
- IWbemDecoupledRegistrar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemDecoupledRegistrar interface


## -description


The 
<b>IWbemDecoupledRegistrar</b> interface associates decoupled providers with WMI. This interface allows a process-hosted provider to define the interoperability lifetime of the interface and to coexist with other providers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemDecoupledRegistrar</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemDecoupledRegistrar</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register">Register</a>
</td>
<td align="left" width="63%">
Registers an object interface with WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-unregister">UnRegister</a>
</td>
<td align="left" width="63%">
Removes an object interface from registration with WMI.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application">Incorporating a Provider in an Application</a>
 

 

