---
UID: NN:netfw.INetFwPolicy2
title: INetFwPolicy2
author: windows-sdk-content
description: To access the firewall policy.
old-location: ics\inetfwpolicy2.htm
tech.root: ics
ms.assetid: ef01a531-ddb0-4eb4-894b-82f613016396
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwPolicy2, INetFwPolicy2 interface [ICS/ICF], INetFwPolicy2 interface [ICS/ICF],described, ics.inetfwpolicy2, netfw/INetFwPolicy2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwPolicy2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwPolicy2 interface


## -description


The <b>INetFwPolicy2</b> interface allows an application or service to access the firewall policy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwPolicy2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetFwPolicy2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwPolicy2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c40e58fd-b372-4d94-bcf1-bad1e84321f7">get_BlockAllInboundTraffic</a>
</td>
<td align="left" width="63%">
Gets the value of the BlockAllInboundTraffic property. This property indicates  whether inbound traffic is blocked for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93f4b508-30db-45a9-a7aa-df4a993dc50b">get_CurrentProfileTypes</a>
</td>
<td align="left" width="63%">
Retrieves the bitmask of the currently active profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9251979-0479-4245-8a29-a161acbf591f">get_DefaultInboundAction</a>
</td>
<td align="left" width="63%">
Gets the value for the default action for inbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/428f8f74-b2b3-4441-accf-be0b877e7c8b">get_DefaultOutboundAction</a>
</td>
<td align="left" width="63%">
Gets the value for the default action for outbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e8cbb09-c146-42e9-9b7c-002e6775bf19">get_ExcludedInterfaces</a>
</td>
<td align="left" width="63%">
Gets the value of the ExcludedInterfaces property.  This property contains the list of interfaces excluded from a specified profile's firewall rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c3ca9dd-a562-454f-bb9a-856beba772f3">get_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Gets the value of the FirewallEnabled property. This property indicates whether the firewall is enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47a18291-398d-459f-b1e8-0bb7c8134e17">get_IsRuleGroupCurrentlyEnabled</a>
</td>
<td align="left" width="63%">
Determines whether a specified group of firewall rules is enabled or disabled for the current profile, considering the firewall's state, BlockAllInboundTraffic state and group policy overrides state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6f27763-6ceb-4bc3-be6f-f02908dc0387">get_IsRuleGroupEnabled</a>
</td>
<td align="left" width="63%">
Determines whether a specified group of firewall rules is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/505c60b9-8359-49eb-aee0-cfa801d9113f">get_LocalPolicyModifyState</a>
</td>
<td align="left" width="63%">
Determines if adding or setting a rule or group of rules will take effect in the current firewall profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/490442a4-3b60-4891-9d0e-71f8d2147999">get_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the NotificationsDisabled property.  This property indicates  whether notifications are enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a3f2846-63c0-4790-b44f-654a34faa974">get_Rules</a>
</td>
<td align="left" width="63%">
Gets the value of the Rules property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc62b295-23b5-40e8-a43a-1b4b67ac0f83">get_ServiceRestriction</a>
</td>
<td align="left" width="63%">
Retrieves the interface to manipulate the Windows Source Hardening (WSH) store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ab9cadf-7ecb-4b3d-a166-b491d89101d7">get_UnicastResponsesToMulticastBroadcastDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the UnicastResponseToMulticastBroadcastDisabled property.  This property indicates whether the firewall should allow unicast incoming responses to outgoing multicast and
   broadcast traffic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c40e58fd-b372-4d94-bcf1-bad1e84321f7">put_BlockAllInboundTraffic</a>
</td>
<td align="left" width="63%">
Sets the value of the BlockALlInboundTraffic property. This property indicates  whether inbound traffic is blocked for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9251979-0479-4245-8a29-a161acbf591f">put_DefaultInboundAction</a>
</td>
<td align="left" width="63%">
Sets the value for the default action for inbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/428f8f74-b2b3-4441-accf-be0b877e7c8b">put_DefaultOutboundAction</a>
</td>
<td align="left" width="63%">
Gets the value for the default action for outbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e8cbb09-c146-42e9-9b7c-002e6775bf19">put_ExcludedInterfaces</a>
</td>
<td align="left" width="63%">
Sets the value of the ExcludedInterfaces property.  This property contains the list of interfaces excluded from a specified profile's firewall rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c3ca9dd-a562-454f-bb9a-856beba772f3">put_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Sets the value of the FirewallEnabled property. This property indicates whether the firewall is enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/490442a4-3b60-4891-9d0e-71f8d2147999">put_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Sets the value of the NotificationsDisabled property. This property indicates  whether notifications are enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ab9cadf-7ecb-4b3d-a166-b491d89101d7">put_UnicastResponsesToMulticastBroadcastDisabled</a>
</td>
<td align="left" width="63%">
Sets the value of the UnicastResponseToMulticastBroadcastDisabled setting. This property indicates whether the firewall should allow unicast incoming responses to outgoing multicast and
   broadcast traffic.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwPolicy2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c40e58fd-b372-4d94-bcf1-bad1e84321f7">BlockAllInboundTraffic</a>


</td>
<td align="left" width="63%">
Access to the property that indicates that inbound traffic should be blocked by the firewall.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/93f4b508-30db-45a9-a7aa-df4a993dc50b">CurrentProfileTypes</a>


</td>
<td align="left" width="63%">
Retrieves the bitmask of the currently active profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d9251979-0479-4245-8a29-a161acbf591f">DefaultInboundAction</a>


</td>
<td align="left" width="63%">
Access to the property that specifies the default action for inbound traffic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/428f8f74-b2b3-4441-accf-be0b877e7c8b">DefaultOutboundAction</a>


</td>
<td align="left" width="63%">
Access to the property that specifies the default action for outbound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fceb9562-b8de-4ccd-9d3e-4a4a4784a35f">EnableRuleGroup</a>


</td>
<td align="left" width="63%">
Enables or disables a specified group of rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0e8cbb09-c146-42e9-9b7c-002e6775bf19">ExcludedInterfaces</a>


</td>
<td align="left" width="63%">
Access to a list of interfaces on which firewall settings are excluded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6c3ca9dd-a562-454f-bb9a-856beba772f3">FirewallEnabled</a>


</td>
<td align="left" width="63%">
Access to the property that indicates whether the firewall is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/490442a4-3b60-4891-9d0e-71f8d2147999">NotificationsDisabled</a>


</td>
<td align="left" width="63%">
Access to the property that indicates whether interactive firewall notifications are disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/420b07ff-e851-41cf-96c4-064430f292a1">RestoreLocalFirewallDefaults</a>


</td>
<td align="left" width="63%">
Restores the local firewall configuration to its default state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1a3f2846-63c0-4790-b44f-654a34faa974">Rules</a>


</td>
<td align="left" width="63%">
Access to the Rules property for this policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc62b295-23b5-40e8-a43a-1b4b67ac0f83">ServiceRestriction</a>


</td>
<td align="left" width="63%">
Access to the Windows Service Hardening (WSH) store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4ab9cadf-7ecb-4b3d-a166-b491d89101d7">UnicastResponsesToMulticastBroadcastDisabled</a>


</td>
<td align="left" width="63%">
Access to the property that indicates whether unicast incoming responses to outgoing multicast and broadcast traffic are disabled.

</td>
</tr>
</table> 


## -remarks



All configuration changes take effect immediately.

The Windows Firewall/Internet Connection Sharing  service must be running to access this interface.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="_com_iunknown">IUnknown</a>
 

 

