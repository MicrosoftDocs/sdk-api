---
UID: NN:netfw.INetFwProfile
title: INetFwProfile (netfw.h)
author: windows-sdk-content
description: The INetFwProfile interface provides access to the firewall settings profile.
old-location: ics\inetfwprofile.htm
tech.root: ics
ms.assetid: 694bbff5-003d-4dde-9a85-f81ca29e6208
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwProfile, INetFwProfile interface [ICS/ICF], INetFwProfile interface [ICS/ICF],described, ics.inetfwprofile, netfw/INetFwProfile
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
 - INetFwProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwProfile interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwProfile</b> interface  provides access to the firewall settings profile.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwProfile</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_authorizedapplications">get_AuthorizedApplications</a>
</td>
<td align="left" width="63%">
Gets the collection containing the  authorized applications for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_exceptionsnotallowed">get_ExceptionsNotAllowed</a>
</td>
<td align="left" width="63%">
Gets the value of the ExceptionsNotAllowed setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_firewallenabled">get_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Gets the value of the FirewallEnabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_globallyopenports">get_GloballyOpenPorts</a>
</td>
<td align="left" width="63%">
Gets the collection containing the  globally open ports for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_icmpsettings">get_IcmpSettings</a>
</td>
<td align="left" width="63%">
Gets the object governing settings for ICMP packets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_notificationsdisabled">get_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the NotificationsDisabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_remoteadminsettings">get_RemoteAdminSettings</a>
</td>
<td align="left" width="63%">
Gets the object containing the remote administration settings .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_services">get_Services</a>
</td>
<td align="left" width="63%">
Gets the collection containing the  services for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_type">get_Type</a>
</td>
<td align="left" width="63%">
Retrieves the type of profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_unicastresponsestomulticastbroadcastdisabled">get_UnicastResponsesToMulticastBroadcastDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the UnicastResponsesToMulticastBroadcastDisabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_exceptionsnotallowed">put_ExceptionsNotAllowed</a>
</td>
<td align="left" width="63%">
Sets the value of the ExceptionsNotAllowed setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_firewallenabled">put_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Sets the value of the FirewallEnabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_notificationsdisabled">put_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Sets the value of the NotificationsDisabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_unicastresponsestomulticastbroadcastdisabled">put_UnicastResponsesToMulticastBroadcastDisabled</a>
</td>
<td align="left" width="63%">
Sets the value of the UnicastResponsesToMulticastBroadcastDisabled setting.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwProfile</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_authorizedapplications">AuthorizedApplications</a>


</td>
<td align="left" width="63%">
Access to the  AuthorizedApplications collection for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_exceptionsnotallowed">ExceptionsNotAllowed</a>


</td>
<td align="left" width="63%">
Access to the  ExceptionsNotAllowed property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_firewallenabled">FirewallEnabled</a>


</td>
<td align="left" width="63%">
Access to the  FirewallEnabled property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_globallyopenports">GloballyOpenPorts</a>


</td>
<td align="left" width="63%">
Access to the  GloballyOpenPorts collection for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_icmpsettings">IcmpSettings</a>


</td>
<td align="left" width="63%">
Access to the  ICMP settings object for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_notificationsdisabled">NotificationsDisabled</a>


</td>
<td align="left" width="63%">
Access to the  NotificationsDisabled property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_remoteadminsettings">RemoteAdminSettings</a>


</td>
<td align="left" width="63%">
Access to the RemoteAdminSettings object for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_services">Services</a>


</td>
<td align="left" width="63%">
Access to the  Services collection for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_type">Type</a>


</td>
<td align="left" width="63%">
Access to the type property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwprofile-get_unicastresponsestomulticastbroadcastdisabled">UnicastResponsesToMulticastBroadcastDisabled</a>


</td>
<td align="left" width="63%">
Access to the UnicastResponsesToMulticastBroadcastDisabled property for this profile.

</td>
</tr>
</table> 


## -remarks



Instances of this interface
are retrieved through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy-get_currentprofile">CurrentProfile</a> property or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy-getprofilebytype">GetProfileByType</a> method
of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy">INetFwPolicy</a> interface.

All configuration changes take
effect immediately.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplications">INetFwAuthorizedApplications</a>



<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nn-netfw-inetfwremoteadminsettings">INetFwRemoteAdminSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservices">InetFwServices</a>
 

 

