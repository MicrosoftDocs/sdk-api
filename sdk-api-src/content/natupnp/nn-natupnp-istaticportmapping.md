---
UID: NN:natupnp.IStaticPortMapping
title: IStaticPortMapping (natupnp.h)
author: windows-sdk-content
description: The IStaticPortMapping interface provides methods to retrieve and change the information for a particular port mapping.
old-location: ics\istaticportmapping.htm
tech.root: ics
ms.assetid: 5013fea2-e767-4600-a10c-6859b7be42e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStaticPortMapping, IStaticPortMapping interface [ICS/ICF], IStaticPortMapping interface [ICS/ICF],described, _ics_istaticportmapping, ics.istaticportmapping, natupnp/IStaticPortMapping
ms.topic: interface
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
 - IStaticPortMapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStaticPortMapping interface


## -description


The 
<b>IStaticPortMapping</b> interface provides methods to retrieve and change the information for a particular port mapping.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStaticPortMapping</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IStaticPortMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStaticPortMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-editdescription">EditDescription</a>
</td>
<td align="left" width="63%">
Changes the description for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-editinternalclient">EditInternalClient</a>
</td>
<td align="left" width="63%">
Changes the internal client for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-editinternalport">EditInternalPort</a>
</td>
<td align="left" width="63%">
Changes the internal port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-enable">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_description">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the description for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_enabled">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves whether this port mapping is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_externalipaddress">get_ExternalIPAddress</a>
</td>
<td align="left" width="63%">
Retrieves the external IP address for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_externalport">get_ExternalPort</a>
</td>
<td align="left" width="63%">
Retrieves the external port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_internalclient">get_InternalClient</a>
</td>
<td align="left" width="63%">
Retrieves the name of the internal client for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_internalport">get_InternalPort</a>
</td>
<td align="left" width="63%">
Retrieves the internal port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nf-natupnp-istaticportmapping-get_protocol">get_Protocol</a>
</td>
<td align="left" width="63%">
Retrieves the protocol for this port mapping.

</td>
</tr>
</table> 


## -remarks



The NAT API with UPnP technology uses the combination of the external port and the protocol to identify the port mapping.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/natupnp/nn-natupnp-istaticportmappingcollection">IStaticPortMappingCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-interfaces">Network Address Translation Traversal Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/network-address-translation-traversal-reference">Network Address Translation Traversal Reference</a>
 

 

