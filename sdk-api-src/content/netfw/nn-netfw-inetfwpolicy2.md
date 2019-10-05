---
UID: NN:netfw.INetFwPolicy2
title: INetFwPolicy2 (netfw.h)
author: windows-sdk-content
description: To access the firewall policy.
old-location: ics\inetfwpolicy2.htm
tech.root: ics
ms.assetid: ef01a531-ddb0-4eb4-894b-82f613016396
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: INetFwPolicy2, INetFwPolicy2 interface [ICS/ICF], INetFwPolicy2 interface [ICS/ICF],described, ics.inetfwpolicy2, netfw/INetFwPolicy2
ms.topic: interface
f1_keywords: 
 - "netfw/INetFwPolicy2"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwPolicy2 interface


## -description


The <b>INetFwPolicy2</b> interface allows an application or service to access the firewall policy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwPolicy2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwPolicy2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_blockallinboundtraffic">get_BlockAllInboundTraffic</a>
</td>
<td align="left" width="63%">
Gets the value of the BlockAllInboundTraffic property. This property indicates  whether inbound traffic is blocked for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">get_CurrentProfileTypes</a>
</td>
<td align="left" width="63%">
Retrieves the bitmask of the currently active profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_defaultinboundaction">get_DefaultInboundAction</a>
</td>
<td align="left" width="63%">
Gets the value for the default action for inbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_defaultoutboundaction">get_DefaultOutboundAction</a>
</td>
<td align="left" width="63%">
Gets the value for the default action for outbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_excludedinterfaces">get_ExcludedInterfaces</a>
</td>
<td align="left" width="63%">
Gets the value of the ExcludedInterfaces property.  This property contains the list of interfaces excluded from a specified profile's firewall rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_firewallenabled">get_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Gets the value of the FirewallEnabled property. This property indicates whether the firewall is enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_isrulegroupcurrentlyenabled">get_IsRuleGroupCurrentlyEnabled</a>
</td>
<td align="left" width="63%">
Determines whether a specified group of firewall rules is enabled or disabled for the current profile, considering the firewall's state, BlockAllInboundTraffic state and group policy overrides state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-isrulegroupenabled">get_IsRuleGroupEnabled</a>
</td>
<td align="left" width="63%">
Determines whether a specified group of firewall rules is enabled or disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_localpolicymodifystate">get_LocalPolicyModifyState</a>
</td>
<td align="left" width="63%">
Determines if adding or setting a rule or group of rules will take effect in the current firewall profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_notificationsdisabled">get_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the NotificationsDisabled property.  This property indicates  whether notifications are enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_rules">get_Rules</a>
</td>
<td align="left" width="63%">
Gets the value of the Rules property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_servicerestriction">get_ServiceRestriction</a>
</td>
<td align="left" width="63%">
Retrieves the interface to manipulate the Windows Source Hardening (WSH) store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_unicastresponsestomulticastbroadcastdisabled">get_UnicastResponsesToMulticastBroadcastDisabled</a>
</td>
<td align="left" width="63%">
Gets the value of the UnicastResponseToMulticastBroadcastDisabled property.  This property indicates whether the firewall should allow unicast incoming responses to outgoing multicast and
   broadcast traffic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_blockallinboundtraffic">put_BlockAllInboundTraffic</a>
</td>
<td align="left" width="63%">
Sets the value of the BlockALlInboundTraffic property. This property indicates  whether inbound traffic is blocked for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_defaultinboundaction">put_DefaultInboundAction</a>
</td>
<td align="left" width="63%">
Sets the value for the default action for inbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_defaultoutboundaction">put_DefaultOutboundAction</a>
</td>
<td align="left" width="63%">
Gets the value for the default action for outbound traffic. It can be either allowed or blocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_excludedinterfaces">put_ExcludedInterfaces</a>
</td>
<td align="left" width="63%">
Sets the value of the ExcludedInterfaces property.  This property contains the list of interfaces excluded from a specified profile's firewall rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_firewallenabled">put_FirewallEnabled</a>
</td>
<td align="left" width="63%">
Sets the value of the FirewallEnabled property. This property indicates whether the firewall is enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_notificationsdisabled">put_NotificationsDisabled</a>
</td>
<td align="left" width="63%">
Sets the value of the NotificationsDisabled property. This property indicates  whether notifications are enabled or disabled for a specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_unicastresponsestomulticastbroadcastdisabled">put_UnicastResponsesToMulticastBroadcastDisabled</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_blockallinboundtraffic">BlockAllInboundTraffic</a>


</td>
<td align="left" width="63%">
Access to the property that indicates that inbound traffic should be blocked by the firewall.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">CurrentProfileTypes</a>


</td>
<td align="left" width="63%">
Retrieves the bitmask of the currently active profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_defaultinboundaction">DefaultInboundAction</a>


</td>
<td align="left" width="63%">
Access to the property that specifies the default action for inbound traffic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_defaultoutboundaction">DefaultOutboundAction</a>


</td>
<td align="left" width="63%">
Access to the property that specifies the default action for outbound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-enablerulegroup">EnableRuleGroup</a>


</td>
<td align="left" width="63%">
Enables or disables a specified group of rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_excludedinterfaces">ExcludedInterfaces</a>


</td>
<td align="left" width="63%">
Access to a list of interfaces on which firewall settings are excluded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_firewallenabled">FirewallEnabled</a>


</td>
<td align="left" width="63%">
Access to the property that indicates whether the firewall is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_notificationsdisabled">NotificationsDisabled</a>


</td>
<td align="left" width="63%">
Access to the property that indicates whether interactive firewall notifications are disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-restorelocalfirewalldefaults">RestoreLocalFirewallDefaults</a>


</td>
<td align="left" width="63%">
Restores the local firewall configuration to its default state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_rules">Rules</a>


</td>
<td align="left" width="63%">
Access to the Rules property for this policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_servicerestriction">ServiceRestriction</a>


</td>
<td align="left" width="63%">
Access to the Windows Service Hardening (WSH) store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_unicastresponsestomulticastbroadcastdisabled">UnicastResponsesToMulticastBroadcastDisabled</a>


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

