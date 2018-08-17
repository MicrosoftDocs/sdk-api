---
UID: NN:netfw.INetFwProfile
title: INetFwProfile
author: windows-sdk-content
description: The INetFwProfile interface provides access to the firewall settings profile.
old-location: ics\inetfwprofile.htm
old-project: ics
ms.assetid: 694bbff5-003d-4dde-9a85-f81ca29e6208
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwProfile, INetFwProfile interface [ICS/ICF], INetFwProfile interface [ICS/ICF],described, ics.inetfwprofile, netfw/INetFwProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: netfw.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
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
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwProfile interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwProfile</b> interface  provides access to the firewall settings profile.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwProfile</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetFwProfile</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/230f7dc0-6afd-4355-a02c-92343d3e10cd">get_AuthorizedApplications</a>
</td>
<td align="left" width="63%">
Gets the collection containing the  authorized applications for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b9eae72-546e-4724-acba-c2f2d9ad1cc6">get_ExceptionsNotAllowed</a>
</td>
<td align="left" width="63%">
Gets the value of the ExceptionsNotAllowed setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde6327d-e3ae-418f-9e8c-76288c120ca0">get_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Gets the value of the FirewallEnabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bb27bb1-7185-4b9a-a529-383e052e5016">get_GloballyOpenPorts</a>
</td>
<td align="left" width="63%">
Gets the collection containing the  globally open ports for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/088be29e-cd1f-4e00-9759-c6e40dca8449">get_IcmpSettings</a>
</td>
<td align="left" width="63%">
Gets the object governing settings for ICMP packets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d184f39d-561f-40aa-99d4-b80e4d0a1aaf">get_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the NotificationsDisabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e05e464-093d-4c25-850a-60e9fad64876">get_RemoteAdminSettings</a>
</td>
<td align="left" width="63%">
Gets the object containing the remote administration settings .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38b32f8e-9aeb-4f63-9880-f393cce185fb">get_Services</a>
</td>
<td align="left" width="63%">
Gets the collection containing the  services for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa3be066-e1f7-47a1-bdde-4bbd79067b1e">get_Type</a>
</td>
<td align="left" width="63%">
Retrieves the type of profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61a0c65e-8dfa-4f3e-a28f-141a72065123">get_UnicastResponsesToMulticastBroadcastDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the UnicastResponsesToMulticastBroadcastDisabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b9eae72-546e-4724-acba-c2f2d9ad1cc6">put_ExceptionsNotAllowed</a>
</td>
<td align="left" width="63%">
Sets the value of the ExceptionsNotAllowed setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde6327d-e3ae-418f-9e8c-76288c120ca0">put_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Sets the value of the FirewallEnabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d184f39d-561f-40aa-99d4-b80e4d0a1aaf">put_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Sets the value of the NotificationsDisabled setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61a0c65e-8dfa-4f3e-a28f-141a72065123">put_UnicastResponsesToMulticastBroadcastDisabled</a>
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

<a href="https://msdn.microsoft.com/230f7dc0-6afd-4355-a02c-92343d3e10cd">AuthorizedApplications</a>


</td>
<td align="left" width="63%">
Access to the  AuthorizedApplications collection for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b9eae72-546e-4724-acba-c2f2d9ad1cc6">ExceptionsNotAllowed</a>


</td>
<td align="left" width="63%">
Access to the  ExceptionsNotAllowed property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cde6327d-e3ae-418f-9e8c-76288c120ca0">FirewallEnabled</a>


</td>
<td align="left" width="63%">
Access to the  FirewallEnabled property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9bb27bb1-7185-4b9a-a529-383e052e5016">GloballyOpenPorts</a>


</td>
<td align="left" width="63%">
Access to the  GloballyOpenPorts collection for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/088be29e-cd1f-4e00-9759-c6e40dca8449">IcmpSettings</a>


</td>
<td align="left" width="63%">
Access to the  ICMP settings object for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d184f39d-561f-40aa-99d4-b80e4d0a1aaf">NotificationsDisabled</a>


</td>
<td align="left" width="63%">
Access to the  NotificationsDisabled property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1e05e464-093d-4c25-850a-60e9fad64876">RemoteAdminSettings</a>


</td>
<td align="left" width="63%">
Access to the RemoteAdminSettings object for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/38b32f8e-9aeb-4f63-9880-f393cce185fb">Services</a>


</td>
<td align="left" width="63%">
Access to the  Services collection for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/aa3be066-e1f7-47a1-bdde-4bbd79067b1e">Type</a>


</td>
<td align="left" width="63%">
Access to the type property for this profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/61a0c65e-8dfa-4f3e-a28f-141a72065123">UnicastResponsesToMulticastBroadcastDisabled</a>


</td>
<td align="left" width="63%">
Access to the UnicastResponsesToMulticastBroadcastDisabled property for this profile.

</td>
</tr>
</table> 


## -remarks



Instances of this interface
are retrieved through the <a href="https://msdn.microsoft.com/2ee59a3e-a4e3-4714-aba7-9d72bfacfb34">CurrentProfile</a> property or <a href="https://msdn.microsoft.com/4c3876cf-40a4-4315-a87a-8fcdf509d48e">GetProfileByType</a> method
of the <a href="https://msdn.microsoft.com/8bfe55b6-c38d-47f8-9160-a304a85eb67f">INetFwPolicy</a> interface.

All configuration changes take
effect immediately.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/70ea2cd1-5422-4db1-ab84-9924dab5623d">INetFwAuthorizedApplications</a>



<a href="https://msdn.microsoft.com/35f34a53-e73b-48be-ac79-9b7ab825c6ad">INetFwRemoteAdminSettings</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/b99464c5-dabc-405a-ad3e-da06a6faef47">InetFwServices</a>
 

 

