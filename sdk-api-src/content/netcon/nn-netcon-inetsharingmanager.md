---
UID: NN:netcon.INetSharingManager
title: INetSharingManager (netcon.h)
author: windows-sdk-content
description: The INetSharingManager interface is the primary interface for the Manager object. INetSharingManager provides methods to determine if sharing is installed, to manage port mappings, and to obtain enumeration interfaces for public and private connections.
old-location: ics\inetsharingmanager.htm
tech.root: ics
ms.assetid: e7009d13-89c2-4fd9-8f6c-dcdc67178598
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetSharingManager, INetSharingManager interface [ICS/ICF], INetSharingManager interface [ICS/ICF],described, _ics_inetsharingmanager, ics.inetsharingmanager, netcon/INetSharingManager
ms.topic: interface
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
 - INetSharingManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetSharingManager interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingManager</b> interface is the primary interface for the Manager object. 
<b>INetSharingManager</b> provides methods to determine if sharing is installed, to manage port mappings, and to obtain enumeration interfaces for public and private connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection">get_EnumEveryConnection</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for all connections in the connections folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_enumprivateconnections">get_EnumPrivateConnections</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for connections that are privately shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_enumpublicconnections">get_EnumPublicConnections</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for connections that are publicly shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">get_INetSharingConfigurationForINetConnection</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface for a specified connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_netconnectionprops">get_NetConnectionProps</a>
</td>
<td align="left" width="63%">
Returns a properties interface for a connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled">get_SharingInstalled</a>
</td>
<td align="left" width="63%">
Reports whether the operating system supports connection sharing.

</td>
</tr>
</table> 


## -remarks



To obtain an enumeration interface for port mappings, use the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface. Then use the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a> method to obtain an 
<a href="https://docs.microsoft.com/windows/desktop/api/netcon/nn-netcon-ienumnetsharingportmapping">IEnumNetSharingPortMapping</a> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

