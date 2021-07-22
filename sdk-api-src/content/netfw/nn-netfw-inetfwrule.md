---
UID: NN:netfw.INetFwRule
title: INetFwRule (netfw.h)
description: To the properties of a rule.
helpviewer_keywords: ["INetFwRule","INetFwRule interface [ICS/ICF]","INetFwRule interface [ICS/ICF]","described","ics.inetfwrule","netfw/INetFwRule"]
old-location: ics\inetfwrule.htm
tech.root: ics
ms.assetid: 59e2a140-bf55-4f0e-bf4b-1a39d3dc0457
ms.date: 12/05/2018
ms.keywords: INetFwRule, INetFwRule interface [ICS/ICF], INetFwRule interface [ICS/ICF],described, ics.inetfwrule, netfw/INetFwRule
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwRule
 - netfw/INetFwRule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule
---

# INetFwRule interface


## -description

The <b>INetFwRule</b> interface provides access to the properties of a rule.

## -inheritance

The <b>INetFwRule</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetFwRule</b> also has these types of members:

## -remarks

Each time you change a property of a rule, Windows Firewall commits the rule and verifies it for correctness. As a result, when you edit a rule, you must perform the steps in a specific order. For example, if you add an ICMP rule, you must first set the protocol to ICMP, then add the rule. If these steps are taken in the opposite order, an error occurs and the change is lost.

If you are editing a TCP port rule and converting it into an ICMP rule, first delete the port, change protocol from TCP to ICMP, and then add the rule.

In order to  retrieve and modify existing rules, instances of this interface must be retrieved through <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules">INetFwRules</a>.  All configuration changes take place immediately.

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
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_name">Name</a>
</td>
<td>Clear text string.</td>
<td>Required. The string must not contain a "|" and it must not be "all".</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_description">Description</a>
</td>
<td>Clear text string.</td>
<td>Optional. The string must not contain a "|".</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_grouping">Grouping</a>
</td>
<td>String in the format "@&lt;dll name&gt;, &lt;resource string identifier&gt;".</td>
<td>Required.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_enabled">Enabled</a>
</td>
<td>Boolean (<b>VARIANT_BOOLEAN</b>).</td>
<td>Optional.  Defaults to false (<b>VARIANT_FALSE</b>) if nothing is specified.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_applicationname">ApplicationName</a>
</td>
<td>Clear text string.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_servicename">ServiceName</a>
</td>
<td>Clear text string.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localports">LocalPorts</a>
</td>
<td>Clear text string containing a list of port numbers.  "RPC" is an acceptable value.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteports">RemotePorts</a>
</td>
<td>Clear text string containing a list of port numbers.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localaddresses">LocalAddresses</a>
</td>
<td>Clear text string containing a list of IPv4 and IPv6 addresses separated by commas.  Range values and"*"are acceptable in this list.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteaddresses">RemoteAddresses</a>
</td>
<td>Clear text string containing a list of IPv4 and IPv6 addresses separated by commas.  Range values and"*"are acceptable in this list.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_protocol">Protocol</a>
</td>
<td>Number.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_profiles">put_Profiles</a>
</td>
<td>String value in the format "type, code". Multiple types and codes can be included in the string by separating each pair with a ";".</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfaces">Interfaces</a>
</td>
<td>Array of strings containing the friendly names of interfaces.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_interfacetypes">InterfaceTypes</a>
</td>
<td>String value. Multiple interface types can be included in the string by separating each value with a ",".  Acceptable values are "RemoteAccess", "Wireless", "Lan", and "All".</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_direction">Direction</a>
</td>
<td>Enumeration.</td>
<td>Optional.  </td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_action">Action</a>
</td>
<td>Enumeration.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_edgetraversal">EdgeTraversal</a>
</td>
<td>Boolean (<b>VARIANT_BOOLEAN</b>).</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_profiles">Profiles</a>
</td>
<td>Enumeration.</td>
<td>Optional.</td>
</tr>
</table>
 

For additional information on each property, please see the corresponding topic.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
