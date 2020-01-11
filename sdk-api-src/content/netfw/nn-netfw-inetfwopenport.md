---
UID: NN:netfw.INetFwOpenPort
title: INetFwOpenPort (netfw.h)
description: The INetFwOpenPort interface provides access to the properties of a port that has been opened in the firewall.
old-location: ics\inetfwopenport.htm
tech.root: ics
ms.assetid: 1a9fd676-b1c0-4be5-9571-d14ac5980af5
ms.date: 12/05/2018
ms.keywords: INetFwOpenPort, INetFwOpenPort interface [ICS/ICF], INetFwOpenPort interface [ICS/ICF],described, ics.inetfwopenport, netfw/INetFwOpenPort
f1_keywords:
- netfw/INetFwOpenPort
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
- INetFwOpenPort
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwOpenPort interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwOpenPort</b> interface provides access to the properties of a port that has been opened in the firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwOpenPort</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwOpenPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwOpenPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_builtin">get_BuiltIn</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the BuiltIn property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_enabled">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_ipversion">get_IpVersion</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Name property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_port">get_Port</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Port property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/port-protocol">get_Protocol</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Protocol property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_remoteaddresses">get_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the  RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_scope">get_Scope</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Scope property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_enabled">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets the contents of the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_ipversion">put_IpVersion</a>
</td>
<td align="left" width="63%">
Sets the contents of the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_name">put_Name</a>
</td>
<td align="left" width="63%">
Sets the contents of the Name property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_port">put_Port</a>
</td>
<td align="left" width="63%">
Sets the contents of the Port property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/port-protocol">put_Protocol</a>
</td>
<td align="left" width="63%">
Sets the contents of the Protocol property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_remoteaddresses">put_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Modifies the contents of the  RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_scope">put_Scope</a>
</td>
<td align="left" width="63%">
Modifies the contents of the Scope property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwOpenPort</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_builtin">BuiltIn</a>


</td>
<td align="left" width="63%">
Accesses the contents of the BuiltIn property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_enabled">Enabled</a>


</td>
<td align="left" width="63%">
Accesses the Enabled property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_ipversion">IpVersion</a>


</td>
<td align="left" width="63%">
Accesses the IpVersion property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_name">Name</a>


</td>
<td align="left" width="63%">
Accesses the Name property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_port">Port</a>


</td>
<td align="left" width="63%">
Accesses the Port property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/port-protocol">Protocol</a>


</td>
<td align="left" width="63%">
Accesses the Protocol property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_remoteaddresses">RemoteAddresses</a>


</td>
<td align="left" width="63%">
Accesses the RemoteAddresses property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_scope">Scope</a>


</td>
<td align="left" width="63%">
Accesses the  Scope property.

</td>
</tr>
</table> 


## -remarks



Ports  with their <b>BuiltIn</b> property set to true (<b>VARIANT_TRUE</b>) are system specified and cannot be removed.

When creating new ports, this interface is supported by the
<b>HNetCfg.FWOpenPort</b> COM object. 

For reading or modifying existing ports,
instances of this interface are retrieved through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFwOpenPorts</a>collection. 

All configuration changes take effect immediately.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenports">INetFwOpenPorts</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

