---
UID: NN:netfw.INetFwRule
title: INetFwRule
author: windows-sdk-content
description: To the properties of a rule.
old-location: ics\inetfwrule.htm
old-project: ics
ms.assetid: 59e2a140-bf55-4f0e-bf4b-1a39d3dc0457
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: INetFwRule, INetFwRule interface [ICS/ICF], INetFwRule interface [ICS/ICF],described, ics.inetfwrule, netfw/INetFwRule
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwRule interface


## -description


The <b>INetFwRule</b> interface provides access to the properties of a rule.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwRule</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetFwRule</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/95c30965-7394-42d8-9e9b-2adb4e5e2986">get_Action</a>
</td>
<td align="left" width="63%">
Retrieves the Action property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ab808fc-39ec-4d3a-9343-4d06f3faa563">get_ApplicationName</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the ApplicationName property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47e5a5ff-d8a7-46e6-aa42-b9e7d544954b">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Description property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4462c39a-27b8-497b-8393-ed63c7e4cc9b">get_Direction</a>
</td>
<td align="left" width="63%">
Retrieves the Direction property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a45a8161-3273-4d43-86bf-34d1b776dbbc">get_EdgeTraversal</a>
</td>
<td align="left" width="63%">
Retrieves the EdgeTraversal property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42533aca-3273-46fa-a9a1-add7f9fde351">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves the Enabled property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/325b0c1d-3988-44ed-931c-6eed835f8c50">get_Grouping</a>
</td>
<td align="left" width="63%">
Retrieves the Grouping property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b1e2e50-7ca1-4a96-a1c3-1f55f51a6a4f">get_IcmpTypesAndCodes</a>
</td>
<td align="left" width="63%">
Retrieves the IcmpTypesAndCodes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f04ac143-bbb7-4676-936e-4282ebf58f56">get_Interfaces</a>
</td>
<td align="left" width="63%">
Retrieves the Interfaces property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2548875c-3c23-4076-9d3d-82bebf5e7718">get_InterfaceTypes</a>
</td>
<td align="left" width="63%">
Retrieves the InterfaceTypes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e95c6545-770b-430f-a1fc-32dcaac0eaa0">get_LocalAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the LocalAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72c4f00c-d5c4-4d93-892b-ec9a63f8df09">get_LocalPorts</a>
</td>
<td align="left" width="63%">
Retrieves the LocalPorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/669ea684-5b00-4b60-8259-fad02cca572b">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the  Name property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98e40140-1df2-439a-9c83-a50f82f65e24">get_Profiles</a>
</td>
<td align="left" width="63%">
Retrieves the Profiles property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16f61a1d-770a-4be9-a43d-10ff9fe276fb">get_Protocol</a>
</td>
<td align="left" width="63%">
Retrieves the Protocol property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/107e8cad-a603-4ac8-aa3c-6a85d47016ef">get_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the RemoteAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6791258-4669-42d9-9551-5c861bfb2b52">get_RemotePorts</a>
</td>
<td align="left" width="63%">
Retrieves the RemotePorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52bcc317-b900-44b6-8ab4-637ffbd74729">get_ServiceName</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the ServiceName property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c30965-7394-42d8-9e9b-2adb4e5e2986">put_Action</a>
</td>
<td align="left" width="63%">
Sets the Action property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ab808fc-39ec-4d3a-9343-4d06f3faa563">put_ApplicationName</a>
</td>
<td align="left" width="63%">
Sets the name of the ApplicationName property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47e5a5ff-d8a7-46e6-aa42-b9e7d544954b">put_Description</a>
</td>
<td align="left" width="63%">
Sets the contents of the Description property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4462c39a-27b8-497b-8393-ed63c7e4cc9b">put_Direction</a>
</td>
<td align="left" width="63%">
Sets the Direction property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a45a8161-3273-4d43-86bf-34d1b776dbbc">put_EdgeTraversal</a>
</td>
<td align="left" width="63%">
Sets the EdgeTraversal property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42533aca-3273-46fa-a9a1-add7f9fde351">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets the Enabled property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/325b0c1d-3988-44ed-931c-6eed835f8c50">put_Grouping</a>
</td>
<td align="left" width="63%">
Sets the Grouping property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b1e2e50-7ca1-4a96-a1c3-1f55f51a6a4f">put_IcmpTypesAndCodes</a>
</td>
<td align="left" width="63%">
Sets the IcmpTypesAndCodes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f04ac143-bbb7-4676-936e-4282ebf58f56">put_Interfaces</a>
</td>
<td align="left" width="63%">
Sets the Interfaces property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2548875c-3c23-4076-9d3d-82bebf5e7718">put_InterfaceTypes</a>
</td>
<td align="left" width="63%">
Sets the InterfaceTypes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e95c6545-770b-430f-a1fc-32dcaac0eaa0">put_LocalAddresses</a>
</td>
<td align="left" width="63%">
Sets the LocalAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72c4f00c-d5c4-4d93-892b-ec9a63f8df09">put_LocalPorts</a>
</td>
<td align="left" width="63%">
Sets the LocalPorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/669ea684-5b00-4b60-8259-fad02cca572b">put_Name</a>
</td>
<td align="left" width="63%">
Sets the contents of the  Name property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98e40140-1df2-439a-9c83-a50f82f65e24">put_Profiles</a>
</td>
<td align="left" width="63%">
Sets the Profiles property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16f61a1d-770a-4be9-a43d-10ff9fe276fb">put_Protocol</a>
</td>
<td align="left" width="63%">
Sets the Protocol property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/107e8cad-a603-4ac8-aa3c-6a85d47016ef">put_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Sets the RemoteAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6791258-4669-42d9-9551-5c861bfb2b52">put_RemotePorts</a>
</td>
<td align="left" width="63%">
Sets the RemotePorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52bcc317-b900-44b6-8ab4-637ffbd74729">put_ServiceName</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/mt270124">Action</a>


</td>
<td align="left" width="63%">
Accesses the Action property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2ab808fc-39ec-4d3a-9343-4d06f3faa563">ApplicationName</a>


</td>
<td align="left" width="63%">
Accesses the ApplicationName property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="63%">
Accesses the Description property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff547596">Direction</a>


</td>
<td align="left" width="63%">
Accesses the Direction property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a45a8161-3273-4d43-86bf-34d1b776dbbc">EdgeTraversal</a>


</td>
<td align="left" width="63%">
Accesses the EdgeTraversal property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a>


</td>
<td align="left" width="63%">
Accesses the Enabled property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/325b0c1d-3988-44ed-931c-6eed835f8c50">Grouping</a>


</td>
<td align="left" width="63%">
Accesses the Grouping property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b1e2e50-7ca1-4a96-a1c3-1f55f51a6a4f">IcmpTypesAndCodes</a>


</td>
<td align="left" width="63%">
Accesses the IcmpTypesAndCodes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>


</td>
<td align="left" width="63%">
Accesses the Interfaces property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2548875c-3c23-4076-9d3d-82bebf5e7718">InterfaceTypes</a>


</td>
<td align="left" width="63%">
Accesses the InterfaceTypes property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e95c6545-770b-430f-a1fc-32dcaac0eaa0">LocalAddresses</a>


</td>
<td align="left" width="63%">
Accesses the LocalAddresses property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/72c4f00c-d5c4-4d93-892b-ec9a63f8df09">LocalPorts</a>


</td>
<td align="left" width="63%">
Accesses the LocalPorts property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="63%">
Accesses the Name property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt764032">Profiles</a>


</td>
<td align="left" width="63%">
Accesses the Profiles property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915742">Protocol</a>


</td>
<td align="left" width="63%">
Accesses the Protocol property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/107e8cad-a603-4ac8-aa3c-6a85d47016ef">RemoteAddresses</a>


</td>
<td align="left" width="63%">
Accesses the RemoteAddresses property of this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e6791258-4669-42d9-9551-5c861bfb2b52">RemotePorts</a>


</td>
<td align="left" width="63%">
Accesses the RemotePorts property for this rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn973169">ServiceName</a>


</td>
<td align="left" width="63%">
Accesses the ServiceName property for this rule.

</td>
</tr>
</table> 


## -remarks



Each time you change a property of a rule, Windows Firewall commits the rule and verifies it for correctness. As a result, when you edit a rule, you must perform the steps in a specific order. For example, if you add an ICMP rule, you must first set the protocol to ICMP, then add the rule. If these steps are taken in the opposite order, an error occurs and the change is lost.

If you are editing a TCP port rule and converting it into an ICMP rule, first delete the port, change protocol from TCP to ICMP, and then add the rule.

In order to  retrieve and modify existing rules, instances of this interface must be retrieved through <a href="https://msdn.microsoft.com/4908a5f2-4093-4f2d-8e68-fe4b2e552b13">INetFwRules</a>.  All configuration changes take place immediately.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>
</td>
<td>Clear text string.</td>
<td>Required. The string must not contain a "|" and it must not be "all".</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>
</td>
<td>Clear text string.</td>
<td>Optional. The string must not contain a "|".</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/325b0c1d-3988-44ed-931c-6eed835f8c50">Grouping</a>
</td>
<td>String in the format "@&lt;dll name&gt;, &lt;resource string identifier&gt;".</td>
<td>Required.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a>
</td>
<td>Boolean (<b>VARIANT_BOOLEAN</b>).</td>
<td>Optional.  Defaults to false (<b>VARIANT_FALSE</b>) if nothing is specified.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2ab808fc-39ec-4d3a-9343-4d06f3faa563">ApplicationName</a>
</td>
<td>Clear text string.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn973169">ServiceName</a>
</td>
<td>Clear text string.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/72c4f00c-d5c4-4d93-892b-ec9a63f8df09">LocalPorts</a>
</td>
<td>Clear text string containing a list of port numbers.  "RPC" is an acceptable value.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e6791258-4669-42d9-9551-5c861bfb2b52">RemotePorts</a>
</td>
<td>Clear text string containing a list of port numbers.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e95c6545-770b-430f-a1fc-32dcaac0eaa0">LocalAddresses</a>
</td>
<td>Clear text string containing a list of IPv4 and IPv6 addresses separated by commas.  Range values and"*"are acceptable in this list.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/107e8cad-a603-4ac8-aa3c-6a85d47016ef">RemoteAddresses</a>
</td>
<td>Clear text string containing a list of IPv4 and IPv6 addresses separated by commas.  Range values and"*"are acceptable in this list.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915742">Protocol</a>
</td>
<td>Number.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/98e40140-1df2-439a-9c83-a50f82f65e24">put_Profiles</a>
</td>
<td>String value in the format "type, code". Multiple types and codes can be included in the string by separating each pair with a ";".</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
</td>
<td>Array of strings containing the friendly names of interfaces.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2548875c-3c23-4076-9d3d-82bebf5e7718">InterfaceTypes</a>
</td>
<td>String value. Multiple interface types can be included in the string by separating each value with a ",".  Acceptable values are "RemoteAccess", "Wireless", "Lan", and "All".</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff547596">Direction</a>
</td>
<td>Enumeration.</td>
<td>Optional.  </td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt270124">Action</a>
</td>
<td>Enumeration.</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a45a8161-3273-4d43-86bf-34d1b776dbbc">EdgeTraversal</a>
</td>
<td>Boolean (<b>VARIANT_BOOLEAN</b>).</td>
<td>Optional.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt764032">Profiles</a>
</td>
<td>Enumeration.</td>
<td>Optional.</td>
</tr>
</table>
 

For additional information on each property, please see the corresponding topic.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="_com_iunknown">IUnknown</a>
 

 

