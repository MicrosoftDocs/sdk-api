---
UID: NN:netcon.INetSharingPortMappingProps
title: INetSharingPortMappingProps (netcon.h)
description: The INetSharingPortMappingProps interface provides methods that retrieve and set the properties of a network connection port mapping.
helpviewer_keywords: ["INetSharingPortMappingProps","INetSharingPortMappingProps interface [ICS/ICF]","INetSharingPortMappingProps interface [ICS/ICF]","described","_ics_inetsharingportmappingprops","ics.inetsharingportmappingprops","netcon/INetSharingPortMappingProps"]
old-location: ics\inetsharingportmappingprops.htm
tech.root: ics
ms.assetid: 9fa20653-5224-4588-89fb-8d4ce07b4235
ms.date: 12/05/2018
ms.keywords: INetSharingPortMappingProps, INetSharingPortMappingProps interface [ICS/ICF], INetSharingPortMappingProps interface [ICS/ICF],described, _ics_inetsharingportmappingprops, ics.inetsharingportmappingprops, netcon/INetSharingPortMappingProps
f1_keywords:
- netcon/INetSharingPortMappingProps
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
- INetSharingPortMappingProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetSharingPortMappingProps interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingPortMappingProps</b> interface provides methods that retrieve and set the properties of a network connection port mapping.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingPortMappingProps</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingPortMappingProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingPortMappingProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_enabled">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieve the port mapping status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_externalport">get_ExternalPort</a>
</td>
<td align="left" width="63%">
Retrieve the  external port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_internalport">get_InternalPort</a>
</td>
<td align="left" width="63%">
Retrieve the internal port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_ipprotocol">get_IPProtocol</a>
</td>
<td align="left" width="63%">
Retrieve the IP protocol associated with this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieve the name for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_options">get_Options</a>
</td>
<td align="left" width="63%">
Retrieve the options for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_targetipaddress">get_TargetIPAddress</a>
</td>
<td align="left" width="63%">
Retrieve the target IP address for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingportmappingprops-get_targetname">get_TargetName</a>
</td>
<td align="left" width="63%">
Retrieve the target name for this port mapping.

</td>
</tr>
</table> 

