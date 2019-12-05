---
UID: NN:natupnp.IUPnPNAT
title: IUPnPNAT (natupnp.h)
description: The IUPnPNAT interface is the primary interface for managing Network Address Translation (NAT) with UPnP. The IUPnPNAT interface provides access directly or indirectly to all the other interfaces in the NAT API with UPnP technology.
old-location: ics\iupnpnat.htm
tech.root: ics
ms.assetid: bfd93967-a514-4301-9b1e-0fee8794d929
ms.date: 12/05/2018
ms.keywords: IUPnPNAT, IUPnPNAT interface [ICS/ICF], IUPnPNAT interface [ICS/ICF],described, _ics_iupnpnat, ics.iupnpnat, natupnp/IUPnPNAT
ms.topic: interface
f1_keywords:
- natupnp/IUPnPNAT
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
- IUPnPNAT
- IUPnPNAT.get_DynamicPortMappingCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPNAT interface


## -description


The 
<b>IUPnPNAT</b> interface is the primary interface for managing Network Address Translation (NAT) with UPnP. The 
<b>IUPnPNAT</b> interface provides access directly or indirectly to all the other interfaces in the NAT API with UPnP technology.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPNAT</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUPnPNAT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPNAT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_DynamicPortMappingCollection</b></td>
<td align="left" width="63%">
This method is not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-iupnpnat-get_nateventmanager">get_NATEventManager</a>
</td>
<td align="left" width="63%">
Establishes callbacks for the NAT to inform the client of changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-iupnpnat-get_staticportmappingcollection">get_StaticPortMappingCollection</a>
</td>
<td align="left" width="63%">
Retrieves the static port mappings collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>
 

 

