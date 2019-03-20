---
UID: NN:netfw.INetFwIcmpSettings
title: INetFwIcmpSettings (netfw.h)
author: windows-sdk-content
description: The INetFwIcmpSettings interface provides access to the settings controlling ICMP packets.
old-location: ics\inetfwicmpsettings.htm
tech.root: ics
ms.assetid: 4eed8f30-4265-4735-a885-83c11b5031e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetFwIcmpSettings, INetFwIcmpSettings interface [ICS/ICF], INetFwIcmpSettings interface [ICS/ICF],described, ics.inetfwicmpsettings, netfw/INetFwIcmpSettings
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwIcmpSettings interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwIcmpSettings</b> interface  provides access to the settings controlling ICMP packets.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwIcmpSettings</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetFwIcmpSettings</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/53ebd01b-71a1-4b4f-b8ad-ede20fae1a7b">get_AllowInboundEchoRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundEchoRequest
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d34c60a-115b-4882-bc41-ea8b3528f9df">get_AllowInboundMaskRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundMaskRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26d9b17c-808d-4d01-921a-9ac435f327db">get_AllowInboundRouterRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundRouterRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6898527d-8556-46ae-b6e4-b1157323d14e">get_AllowInboundTimestampRequest</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowInboundTimestampRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da3719a3-67b3-44a8-9cf8-0062f476bb2c">get_AllowOutboundDestinationUnreachable</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundDestinationUnreachable property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057b2f45-1752-4f6d-a6a6-9871e20cd13a">get_AllowOutboundPacketTooBig</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundPacketTooBig
           property. Type common to IPv6 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/496374e7-9f89-43e3-bb59-184ba4c611be">get_AllowOutboundParameterProblem</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundParameterProblem
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a70cdff7-5e93-4120-9000-424a91d522ea">get_AllowOutboundSourceQuench</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundSourceQuench
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0a78d16-ce10-4978-bd66-e4841a4c52b6">get_AllowOutboundTimeExceeded</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowOutboundTimeExceeded property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d4d5e8c-8903-46f6-ba41-a7a00ac50312">get_AllowRedirect</a>
</td>
<td align="left" width="63%">
Gets the value of the AllowRedirect
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53ebd01b-71a1-4b4f-b8ad-ede20fae1a7b">put_AllowInboundEchoRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundEchoRequest
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d34c60a-115b-4882-bc41-ea8b3528f9df">put_AllowInboundMaskRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundMaskRequest property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26d9b17c-808d-4d01-921a-9ac435f327db">put_AllowInboundRouterRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundRouterRequest property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6898527d-8556-46ae-b6e4-b1157323d14e">put_AllowInboundTimestampRequest</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowInboundTimestampRequest property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da3719a3-67b3-44a8-9cf8-0062f476bb2c">put_AllowOutboundDestinationUnreachable</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundDestinationUnreachable property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057b2f45-1752-4f6d-a6a6-9871e20cd13a">put_AllowOutboundPacketTooBig</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundPacketTooBig property. Type common to IPv6 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/496374e7-9f89-43e3-bb59-184ba4c611be">put_AllowOutboundParameterProblem</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundParameterProblem
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a70cdff7-5e93-4120-9000-424a91d522ea">put_AllowOutboundSourceQuench</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundSourceQuench property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0a78d16-ce10-4978-bd66-e4841a4c52b6">put_AllowOutboundTimeExceeded</a>
</td>
<td align="left" width="63%">
Sets the value of the AllowOutboundTimeExceeded property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d4d5e8c-8903-46f6-ba41-a7a00ac50312">put_AllowRedirect</a>
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

<a href="https://msdn.microsoft.com/53ebd01b-71a1-4b4f-b8ad-ede20fae1a7b">AllowInboundEchoRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundEchoRequest
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5d34c60a-115b-4882-bc41-ea8b3528f9df">AllowInboundMaskRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundMaskRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/26d9b17c-808d-4d01-921a-9ac435f327db">AllowInboundRouterRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundRouterRequest
           Property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6898527d-8556-46ae-b6e4-b1157323d14e">AllowInboundTimestampRequest</a>


</td>
<td align="left" width="63%">
Accesses the AllowInboundTimestampRequest
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/da3719a3-67b3-44a8-9cf8-0062f476bb2c">AllowOutboundDestinationUnreachable</a>


</td>
<td align="left" width="63%">
Accesses the  AllowOutboundDestinationUnreachable property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/057b2f45-1752-4f6d-a6a6-9871e20cd13a">AllowOutboundPacketTooBig</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundPacketTooBig
           property. Type common to IPv6 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/496374e7-9f89-43e3-bb59-184ba4c611be">AllowOutboundParameterProblem</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundParameterProblem
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a70cdff7-5e93-4120-9000-424a91d522ea">AllowOutboundSourceQuench</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundSourceQuench
           property. Type common to IPv4 only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b0a78d16-ce10-4978-bd66-e4841a4c52b6">AllowOutboundTimeExceeded</a>


</td>
<td align="left" width="63%">
Accesses the AllowOutboundTimeExceeded
           property. Type common to IPv4 and IPv6.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2d4d5e8c-8903-46f6-ba41-a7a00ac50312">AllowRedirect</a>


</td>
<td align="left" width="63%">
Accesses the  AllowRedirect property. Type common to IPv4 and IPv6.

</td>
</tr>
</table> 


## -remarks



Instances of this interface
are retrieved through the <a href="https://msdn.microsoft.com/088be29e-cd1f-4e00-9759-c6e40dca8449">IcmpSettings</a> property of the INetFwProfile interface.

Because the methods and properties of this interface enable all rules belonging to a given ICMP type, enabling a rule may enable rules from other groups as well.

All configuration changes take
effect immediately.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/088be29e-cd1f-4e00-9759-c6e40dca8449">INetFwProfile.IcmpSettings</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

