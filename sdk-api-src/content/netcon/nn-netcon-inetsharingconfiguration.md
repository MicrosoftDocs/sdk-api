---
UID: NN:netcon.INetSharingConfiguration
title: INetSharingConfiguration (netcon.h)
author: windows-sdk-content
description: The INetSharingConfiguration interface provides methods to manage connection sharing, port mapping, and Internet Connection Firewall.
old-location: ics\inetsharingconfiguration.htm
tech.root: ics
ms.assetid: 3ed1a3ae-87af-4415-b149-c66ae65cd053
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetSharingConfiguration, INetSharingConfiguration interface [ICS/ICF], INetSharingConfiguration interface [ICS/ICF],described, _ics_inetsharingconfiguration, ics.inetsharingconfiguration, netcon/INetSharingConfiguration
ms.topic: interface
f1_keywords: 
 - "netcon/INetSharingConfiguration"
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
 - INetSharingConfiguration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetSharingConfiguration interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingConfiguration</b> interface provides methods to manage connection sharing, port mapping, and Internet Connection Firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingConfiguration</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">AddPortMapping</a>
</td>
<td align="left" width="63%">
Adds a service-port mapping for this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-disableinternetfirewall">DisableInternetFirewall</a>
</td>
<td align="left" width="63%">
Disables Internet Connection Firewall on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing">DisableSharing</a>
</td>
<td align="left" width="63%">
Disables sharing on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-enableinternetfirewall">EnableInternetFirewall</a>
</td>
<td align="left" width="63%">
Enables Internet Connection Firewall on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing">EnableSharing</a>
</td>
<td align="left" width="63%">
Enables sharing on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">EnumPortMappings</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nn-netcon-ienumnetsharingportmapping">IEnumNetSharingPortMapping</a> interface for this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_internetfirewallenabled">get_InternetFirewallEnabled</a>
</td>
<td align="left" width="63%">
Determines whether Internet Connection Firewall is enabled on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_sharingconnectiontype">get_SharingConnectionType</a>
</td>
<td align="left" width="63%">
Determines the type of sharing on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_sharingenabled">get_SharingEnabled</a>
</td>
<td align="left" width="63%">
Determines whether sharing is enabled on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-removeportmapping">RemovePortMapping</a>
</td>
<td align="left" width="63%">
Removes a service-port mapping for this connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

