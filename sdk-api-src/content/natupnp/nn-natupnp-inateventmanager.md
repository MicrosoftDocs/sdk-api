---
UID: NN:natupnp.INATEventManager
title: INATEventManager (natupnp.h)
description: The INATEventManager interface provides methods for NAT applications with UPnP technology to register callback interfaces with the NAT. The system calls the methods in these interfaces when the configuration of the NAT changes.helpviewer_keywords: ["INATEventManager","INATEventManager interface [ICS/ICF]","INATEventManager interface [ICS/ICF]","described","_ics_inateventmanager","ics.inateventmanager","natupnp/INATEventManager"]
old-location: ics\inateventmanager.htm
tech.root: ics
ms.assetid: 18c5df1a-e57e-4f44-bac5-a5861f939673
ms.date: 12/05/2018
ms.keywords: INATEventManager, INATEventManager interface [ICS/ICF], INATEventManager interface [ICS/ICF],described, _ics_inateventmanager, ics.inateventmanager, natupnp/INATEventManager
f1_keywords:
- natupnp/INATEventManager
dev_langs:
- c++
req.header: natupnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Hnetcfg.dll
api_name:
- INATEventManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INATEventManager interface


## -description


The 
<b>INATEventManager</b> interface provides methods for NAT applications with UPnP technology to register callback interfaces with the NAT. The system calls the methods in these interfaces when the configuration of the NAT changes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INATEventManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INATEventManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INATEventManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-inateventmanager-put_externalipaddresscallback">put_ExternalIPAddressCallback</a>
</td>
<td align="left" width="63%">
Registers the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inatexternalipaddresscallback">INATExternalIPAddressCallback</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-inateventmanager-put_numberofentriescallback">put_NumberOfEntriesCallback</a>
</td>
<td align="left" width="63%">
Registers the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nn-natupnp-inatnumberofentriescallback">INATNumberOfEntriesCallback</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>
 

 

