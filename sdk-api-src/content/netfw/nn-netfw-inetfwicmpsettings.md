---
UID: NN:netfw.INetFwIcmpSettings
title: INetFwIcmpSettings (netfw.h)
description: The INetFwIcmpSettings interface provides access to the settings controlling ICMP packets.
old-location: ics\inetfwicmpsettings.htm
tech.root: ics
ms.assetid: 4eed8f30-4265-4735-a885-83c11b5031e5
ms.date: 12/05/2018
ms.keywords: INetFwIcmpSettings, INetFwIcmpSettings interface [ICS/ICF], INetFwIcmpSettings interface [ICS/ICF],described, ics.inetfwicmpsettings, netfw/INetFwIcmpSettings
ms.topic: interface
f1_keywords:
- netfw/INetFwIcmpSettings
dev_langs:
- c++
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FirewallAPI.dll
- Hnetcfg.dll
api_name:
- INetFwIcmpSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwIcmpSettings interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwIcmpSettings</b> interface  provides access to the settings controlling ICMP packets.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwIcmpSettings</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwIcmpSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwIcmpSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundechorequest">get_AllowInboundEchoRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundEchoRequest
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundmaskrequest">get_AllowInboundMaskRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundMaskRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundrouterrequest">get_AllowInboundRouterRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundRouterRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundtimestamprequest">get_AllowInboundTimestampRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundTimestampRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutbounddestinationunreachable">get_AllowOutboundDestinationUnreachable</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundDestinationUnreachable property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundpackettoobig">get_AllowOutboundPacketTooBig</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundPacketTooBig
           property. Type common to IPv6 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundparameterproblem">get_AllowOutboundParameterProblem</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundParameterProblem
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundsourcequench">get_AllowOutboundSourceQuench</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundSourceQuench
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundtimeexceeded">get_AllowOutboundTimeExceeded</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundTimeExceeded property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowredirect">get_AllowRedirect</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowRedirect
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundechorequest">put_AllowInboundEchoRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundEchoRequest
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundmaskrequest">put_AllowInboundMaskRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundMaskRequest property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundrouterrequest">put_AllowInboundRouterRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundRouterRequest property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundtimestamprequest">put_AllowInboundTimestampRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundTimestampRequest property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutbounddestinationunreachable">put_AllowOutboundDestinationUnreachable</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundDestinationUnreachable property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundpackettoobig">put_AllowOutboundPacketTooBig</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundPacketTooBig property. Type common to IPv6 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundparameterproblem">put_AllowOutboundParameterProblem</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundParameterProblem
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundsourcequench">put_AllowOutboundSourceQuench</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundSourceQuench property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundtimeexceeded">put_AllowOutboundTimeExceeded</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundTimeExceeded property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowredirect">put_AllowRedirect</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowRedirect property. Type common to IPv4 and IPv6.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwIcmpSettings</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundechorequest">AllowInboundEchoRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundEchoRequest
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundmaskrequest">AllowInboundMaskRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundMaskRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundrouterrequest">AllowInboundRouterRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundRouterRequest
           Property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowinboundtimestamprequest">AllowInboundTimestampRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundTimestampRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutbounddestinationunreachable">AllowOutboundDestinationUnreachable</a>


</td>
<td align="left" width="63%">
Accesses the  AllowOutboundDestinationUnreachable property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundpackettoobig">AllowOutboundPacketTooBig</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundPacketTooBig
           property. Type common to IPv6 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundparameterproblem">AllowOutboundParameterProblem</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundParameterProblem
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundsourcequench">AllowOutboundSourceQuench</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundSourceQuench
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowoutboundtimeexceeded">AllowOutboundTimeExceeded</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundTimeExceeded
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwicmpsettings-get_allowredirect">AllowRedirect</a>


</td>
<td align="left" width="63%">
Accesses the  AllowRedirect property. Type common to IPv4 and IPv6.

</td>
</tr>
</table> 


## -remarks



Instances of this interface
are retrieved through the <a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_icmpsettings">IcmpSettings</a> property of the INetFwProfile interface.

Because the methods and properties of this interface enable all rules belonging to a given ICMP type, enabling a rule may enable rules from other groups as well.

All configuration changes take
effect immediately.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_icmpsettings">INetFwProfile.IcmpSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

