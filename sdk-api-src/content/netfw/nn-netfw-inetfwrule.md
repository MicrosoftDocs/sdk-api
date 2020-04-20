---
UID: NN:netfw.INetFwRule
title: INetFwRule (netfw.h)
description: To the properties of a rule.helpviewer_keywords: ["INetFwRule","INetFwRule interface [ICS/ICF]","INetFwRule interface [ICS/ICF]","described","ics.inetfwrule","netfw/INetFwRule"]
old-location: ics\inetfwrule.htm
tech.root: ics
ms.assetid: 59e2a140-bf55-4f0e-bf4b-1a39d3dc0457
ms.date: 12/05/2018
ms.keywords: INetFwRule, INetFwRule interface [ICS/ICF], INetFwRule interface [ICS/ICF],described, ics.inetfwrule, netfw/INetFwRule
f1_keywords:
- netfw/INetFwRule
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
- INetFwRule
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwRule interface


## -description


The <b>INetFwRule</b> interface provides access to the properties of a rule.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRule</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwRule</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwRule</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_action">get_Action</a>
</td>
<td align="left" width="63%">
Retrieves the Action property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_applicationname">get_ApplicationName</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the ApplicationName property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_description">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Description property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_direction">get_Direction</a>
</td>
<td align="left" width="63%">
Retrieves the Direction property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_edgetraversal">get_EdgeTraversal</a>
</td>
<td align="left" width="63%">
Retrieves the EdgeTraversal property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_enabled">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves the Enabled property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_grouping">get_Grouping</a>
</td>
<td align="left" width="63%">
Retrieves the Grouping property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_icmptypesandcodes">get_IcmpTypesAndCodes</a>
</td>
<td align="left" width="63%">
Retrieves the IcmpTypesAndCodes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfaces">get_Interfaces</a>
</td>
<td align="left" width="63%">
Retrieves the Interfaces property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfacetypes">get_InterfaceTypes</a>
</td>
<td align="left" width="63%">
Retrieves the InterfaceTypes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localaddresses">get_LocalAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the LocalAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localports">get_LocalPorts</a>
</td>
<td align="left" width="63%">
Retrieves the LocalPorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the  Name property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_profiles">get_Profiles</a>
</td>
<td align="left" width="63%">
Retrieves the Profiles property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_protocol">get_Protocol</a>
</td>
<td align="left" width="63%">
Retrieves the Protocol property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteaddresses">get_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the RemoteAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteports">get_RemotePorts</a>
</td>
<td align="left" width="63%">
Retrieves the RemotePorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_servicename">get_ServiceName</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the ServiceName property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_action">put_Action</a>
</td>
<td align="left" width="63%">
Sets the Action property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_applicationname">put_ApplicationName</a>
</td>
<td align="left" width="63%">
Sets the name of the ApplicationName property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_description">put_Description</a>
</td>
<td align="left" width="63%">
Sets the contents of the Description property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_direction">put_Direction</a>
</td>
<td align="left" width="63%">
Sets the Direction property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_edgetraversal">put_EdgeTraversal</a>
</td>
<td align="left" width="63%">
Sets the EdgeTraversal property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_enabled">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets the Enabled property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_grouping">put_Grouping</a>
</td>
<td align="left" width="63%">
Sets the Grouping property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_icmptypesandcodes">put_IcmpTypesAndCodes</a>
</td>
<td align="left" width="63%">
Sets the IcmpTypesAndCodes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfaces">put_Interfaces</a>
</td>
<td align="left" width="63%">
Sets the Interfaces property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfacetypes">put_InterfaceTypes</a>
</td>
<td align="left" width="63%">
Sets the InterfaceTypes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localaddresses">put_LocalAddresses</a>
</td>
<td align="left" width="63%">
Sets the LocalAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localports">put_LocalPorts</a>
</td>
<td align="left" width="63%">
Sets the LocalPorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_name">put_Name</a>
</td>
<td align="left" width="63%">
Sets the contents of the  Name property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_profiles">put_Profiles</a>
</td>
<td align="left" width="63%">
Sets the Profiles property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_protocol">put_Protocol</a>
</td>
<td align="left" width="63%">
Sets the Protocol property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteaddresses">put_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Sets the RemoteAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteports">put_RemotePorts</a>
</td>
<td align="left" width="63%">
Sets the RemotePorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_servicename">put_ServiceName</a>
</td>
<td align="left" width="63%">
Sets the contents of the ServiceName property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRule</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_action">Action</a>


</td>
<td align="left" width="63%">
Accesses the Action property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_applicationname">ApplicationName</a>


</td>
<td align="left" width="63%">
Accesses the ApplicationName property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_description">Description</a>


</td>
<td align="left" width="63%">
Accesses the Description property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_direction">Direction</a>


</td>
<td align="left" width="63%">
Accesses the Direction property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_edgetraversal">EdgeTraversal</a>


</td>
<td align="left" width="63%">
Accesses the EdgeTraversal property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_enabled">Enabled</a>


</td>
<td align="left" width="63%">
Accesses the Enabled property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_grouping">Grouping</a>


</td>
<td align="left" width="63%">
Accesses the Grouping property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_icmptypesandcodes">IcmpTypesAndCodes</a>


</td>
<td align="left" width="63%">
Accesses the IcmpTypesAndCodes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfaces">Interfaces</a>


</td>
<td align="left" width="63%">
Accesses the Interfaces property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfacetypes">InterfaceTypes</a>


</td>
<td align="left" width="63%">
Accesses the InterfaceTypes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localaddresses">LocalAddresses</a>


</td>
<td align="left" width="63%">
Accesses the LocalAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localports">LocalPorts</a>


</td>
<td align="left" width="63%">
Accesses the LocalPorts property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_name">Name</a>


</td>
<td align="left" width="63%">
Accesses the Name property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_profiles">Profiles</a>


</td>
<td align="left" width="63%">
Accesses the Profiles property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_protocol">Protocol</a>


</td>
<td align="left" width="63%">
Accesses the Protocol property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteaddresses">RemoteAddresses</a>


</td>
<td align="left" width="63%">
Accesses the RemoteAddresses property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteports">RemotePorts</a>


</td>
<td align="left" width="63%">
Accesses the RemotePorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_servicename">ServiceName</a>


</td>
<td align="left" width="63%">
Accesses the ServiceName property for this rule.

</td>
</tr>
</table> 


## -remarks



Each time you change a property of a rule, Windows Firewall commits the rule and verifies it for correctness. As a result, when you edit a rule, you must perform the steps in a specific order. For example, if you add an ICMP rule, you must first set the protocol to ICMP, then add the rule. If these steps are taken in the opposite order, an error occurs and the change is lost.

If you are editing a TCP port rule and converting it into an ICMP rule, first delete the port, change protocol from TCP to ICMP, and then add the rule.

In order to  retrieve and modify existing rules, instances of this interface must be retrieved through <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules">INetFwRules</a>.  All configuration changes take place immediately.

When accessing the properties of a  	rule, keep in mind that there may be a small time lag before a newly-added rule is applied.

Properties are used to create firewall rules.  Many of the properties can be used in order to create very specific firewall rules.

<table>
<tr>
<th>Property</th>
<th>Type and format</th>
<th>Constraints</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_name">Name</a>
</td>
<td>Clear text string.</td>
<td>Required. The string must not contain a "|" and it must not be "all".</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_description">Description</a>
</td>
<td>Clear text string.</td>
<td>Optional. The string must not contain a "|".</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_grouping">Grouping</a>
</td>
<td>String in the format "@&lt;dll name&gt;, &lt;resource string identifier&gt;".</td>
<td>Required.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_enabled">Enabled</a>
</td>
<td>Boolean (<b>VARIANT_BOOLEAN</b>).</td>
<td>Optional.  Defaults to false (<b>VARIANT_FALSE</b>) if nothing is specified.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_applicationname">ApplicationName</a>
</td>
<td>Clear text string.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_servicename">ServiceName</a>
</td>
<td>Clear text string.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localports">LocalPorts</a>
</td>
<td>Clear text string containing a list of port numbers.  "RPC" is an acceptable value.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteports">RemotePorts</a>
</td>
<td>Clear text string containing a list of port numbers.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localaddresses">LocalAddresses</a>
</td>
<td>Clear text string containing a list of IPv4 and IPv6 addresses separated by commas.  Range values and"*"are acceptable in this list.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteaddresses">RemoteAddresses</a>
</td>
<td>Clear text string containing a list of IPv4 and IPv6 addresses separated by commas.  Range values and"*"are acceptable in this list.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_protocol">Protocol</a>
</td>
<td>Number.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_profiles">put_Profiles</a>
</td>
<td>String value in the format "type, code". Multiple types and codes can be included in the string by separating each pair with a ";".</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfaces">Interfaces</a>
</td>
<td>Array of strings containing the friendly names of interfaces.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfacetypes">InterfaceTypes</a>
</td>
<td>String value. Multiple interface types can be included in the string by separating each value with a ",".  Acceptable values are "RemoteAccess", "Wireless", "Lan", and "All".</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_direction">Direction</a>
</td>
<td>Enumeration.</td>
<td>Optional.  </td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_action">Action</a>
</td>
<td>Enumeration.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_edgetraversal">EdgeTraversal</a>
</td>
<td>Boolean (<b>VARIANT_BOOLEAN</b>).</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_profiles">Profiles</a>
</td>
<td>Enumeration.</td>
<td>Optional.</td>
</tr>
</table>
 

For additional information on each property, please see the corresponding topic.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

