---
UID: NN:netcon.INetSharingPortMapping
title: INetSharingPortMapping (netcon.h)
description: The INetSharingPortMapping interface provides methods for managing a particular port mapping.
helpviewer_keywords: ["INetSharingPortMapping","INetSharingPortMapping interface [ICS/ICF]","INetSharingPortMapping interface [ICS/ICF]","described","_ics_inetsharingportmapping","ics.inetsharingportmapping","netcon/INetSharingPortMapping"]
old-location: ics\inetsharingportmapping.htm
tech.root: ics
ms.assetid: 236608c3-061e-4db0-96df-25d263b6463b
ms.date: 12/05/2018
ms.keywords: INetSharingPortMapping, INetSharingPortMapping interface [ICS/ICF], INetSharingPortMapping interface [ICS/ICF],described, _ics_inetsharingportmapping, ics.inetsharingportmapping, netcon/INetSharingPortMapping
f1_keywords:
- netcon/INetSharingPortMapping
dev_langs:
- c++
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
- INetSharingPortMapping
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetSharingPortMapping interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingPortMapping</b> interface provides methods for managing a particular port mapping.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPortMapping</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingPortMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPortMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmapping-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmapping-disable">Disable</a>
</td>
<td align="left" width="63%">
Disables the port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmapping-enable">Enable</a>
</td>
<td align="left" width="63%">
Enables the port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmapping-get_properties">get_Properties</a>
</td>
<td align="left" width="63%">
Retrieves the properties for the port mapping.

</td>
</tr>
</table> 


## -remarks



Use the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">INetSharingConfiguration::AddPortMapping</a> and 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a> methods to obtain 
<b>INetSharingPortMapping</b> interfaces.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">INetSharingConfiguration::AddPortMapping</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

