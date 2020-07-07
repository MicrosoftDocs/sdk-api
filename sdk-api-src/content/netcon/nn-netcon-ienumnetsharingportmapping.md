---
UID: NN:netcon.IEnumNetSharingPortMapping
title: IEnumNetSharingPortMapping (netcon.h)
description: The IEnumNetSharingPortMapping interface provides methods to enumerate the port mappings for a particular connection.
helpviewer_keywords: ["IEnumNetSharingPortMapping","IEnumNetSharingPortMapping interface [ICS/ICF]","IEnumNetSharingPortMapping interface [ICS/ICF]","described","_ics_ienumnetsharingportmapping","ics.ienumnetsharingportmapping","netcon/IEnumNetSharingPortMapping"]
old-location: ics\ienumnetsharingportmapping.htm
tech.root: ics
ms.assetid: 68334bd2-353f-457d-a2c7-1271816f10f5
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingPortMapping, IEnumNetSharingPortMapping interface [ICS/ICF], IEnumNetSharingPortMapping interface [ICS/ICF],described, _ics_ienumnetsharingportmapping, ics.ienumnetsharingportmapping, netcon/IEnumNetSharingPortMapping
f1_keywords:
- netcon/IEnumNetSharingPortMapping
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
- IEnumNetSharingPortMapping
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumNetSharingPortMapping interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingPortMapping</b> interface provides methods to enumerate the port mappings for a particular connection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumNetSharingPortMapping</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetSharingPortMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumNetSharingPortMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingportmapping-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingportmapping-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of port mappings from this enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingportmapping-reset">Reset</a>
</td>
<td align="left" width="63%">
Causes subsequent calls to operate from the beginning of the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-ienumnetsharingportmapping-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of port mappings in this enumeration.

</td>
</tr>
</table> 


## -remarks



To obtain an enumeration interface for port mappings, use the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface. Then use the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a> method to obtain an 
<b>IEnumNetSharingPortMapping</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

