---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# INetwork interface


## -description


The <b>INetwork</b> interface represents a network on the local machine. It can also represent a collection of network connections with a similar network signature.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetwork</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INetwork</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetwork</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a57c6ad-8c6c-4ef0-a731-463a5d7e325f">GetCategory</a>
</td>
<td align="left" width="63%">
Returns the category of a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04191757-7d9f-4211-a311-4863d62bd0a5">GetConnectivity</a>
</td>
<td align="left" width="63%">
Returns the connectivity state of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a description string for the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca23d7c0-fe25-4375-bd2c-6c2ccae56548">GetDomainType</a>
</td>
<td align="left" width="63%">
Returns the type of network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0dd843e-5bba-4504-b0af-26c0c1ee73a9">GetName</a>
</td>
<td align="left" width="63%">
Returns the name of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc599537-3c31-4674-81d0-608cadae3e61">GetNetworkConnections</a>
</td>
<td align="left" width="63%">
Returns an enumeration of all network connections for a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2012295-d443-434f-8fe8-b6e38e7cac74">GetNetworkId</a>
</td>
<td align="left" width="63%">
Returns the unique identifier of a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/607ce0be-fe7e-4969-b9d0-db1def054f67">GetTimeCreatedAndConnected</a>
</td>
<td align="left" width="63%">
Returns the local date and time when the network was created and connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cbaa23e-f57c-4608-814b-9ccff1ec515f">SetCategory</a>
</td>
<td align="left" width="63%">
Sets the category of a network. Administrative privileges are needed for this API call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d21fc8ca-d097-4099-8c64-f449d1fd49ef">SetDescription</a>
</td>
<td align="left" width="63%">
Sets a new description for the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7495e26f-b7cf-4abd-ab7d-82b0d4bd4d87">SetName</a>
</td>
<td align="left" width="63%">
Sets or renames the network. This change occurs immediately.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetwork</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/24bfcd98-b9c3-44f5-9f7b-13c05dcc8974">get_IsConnected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the network has any network connectivity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/12df15aa-64df-426f-aa41-12b96fc35e55">get_IsConnectedToInternet</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies if the network has internet connectivity.

</td>
</tr>
</table> 


## -remarks



The COM Object that implements <b>INetwork</b> also implements a property bag for additional properties. To get access to this property bag you can use the <b>INetwork</b> interface and <a href="Http://go.microsoft.com/fwlink/p/?linkid=83937">QueryInterface</a> for <a href="Http://go.microsoft.com/fwlink/p/?linkid=83936">IPropertyBag</a>. The property bag on this COM Object contains the following properties:

<table>
<tr>
<th>Parameter</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>NA_DomainAuthenticationFailed</td>
<td>VT_BOOL</td>
<td>Specifies that a domain network is not able to authenticate against the domain controller.</td>
</tr>
<tr>
<td>NA_NetworkClass</td>
<td>
<a href="https://msdn.microsoft.com/397602c6-efc5-454a-999b-26ea26cb56cd">NLM_NETWORK_CLASS</a> value stored as VT_UINT </td>
<td>Specifies the class of network. Possible values include:<ul>
<li>
NLM_NETWORK_IDENTIFYING     (0x01)

This is the special "Identifying" network. No properties on this network class can be changed.

</li>
<li>
NLM_NETWORK_IDENTIFIED       (0x02)

This is an Identified network.

</li>
<li>
NLM_NETWORK_UNIDENTIFIED    (0x03)

This is the special "Unidentified" network. The category of this network can be changed, but it will not persist when the network is disconnected.

</li>
</ul>
</td>
</tr>
<tr>
<td>
NA_InternetConnectivityV4 

or

NA_InternetConnectivityV6 

</td>
<td>
<a href="https://msdn.microsoft.com/5B1DB4D5-6F69-4628-AEAF-E280E9B4E71C">NLM_INTERNET_CONNECTIVITY</a> value stored as VT_UINT</td>
<td>
Provides details regarding IPv4 or IPv6 network connectivity. Possible values include:<ul>
<li>
NLM_INTERNET_CONNECTIVITY_WEBHIJACK (0x1)

The detected network is a hotspot. For example, when connected to a coffee Wi-Fi hotspot network and the local HTTP traffic is being redirected to a captive portal, this flag will be set.

</li>
<li>
NLM_INTERNET_CONNECTIVITY_PROXIED (0x2)

The detected network has a proxy configuration. For example, when connected to a corporate network using a proxy for HTTP access, this flag will be set.

</li>
<li>
NLM_INTERNET_CONNECTIVITY_CORPORATE (0x4)

The machine has been configured for Direct Access and access is detected to the corporate domain network Direct Access has been configured for.

</li>
</ul>


</td>
</tr>
<tr>
<td>NA_NameSetByPolicy</td>
<td>VT_BOOL</td>
<td>The name of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_IconSetByPolicy</td>
<td>VT_BOOL</td>
<td>The icon of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_DescriptionSetByPolicy</td>
<td>VT_BOOL</td>
<td>The description of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_CategorySetByPolicy</td>
<td>VT_BOOL</td>
<td>The category of the network has been set by group policy.</td>
</tr>
<tr>
<td>NA_NameReadOnly</td>
<td>VT_BOOL</td>
<td>The name of the network is read only.</td>
</tr>
<tr>
<td>NA_IconReadOnly</td>
<td>VT_BOOL</td>
<td>The icon of the network is read only.</td>
</tr>
<tr>
<td>NA_DescriptionReadOnly</td>
<td>VT_BOOL</td>
<td>The description of the network is read only.</td>
</tr>
<tr>
<td>NA_CategoryReadOnly</td>
<td>VT_BOOL</td>
<td>The category of the network is read only.</td>
</tr>
<tr>
<td>NA_AllowMerge</td>
<td>VT_BOOL</td>
<td>The network can be merged with another network.</td>
</tr>
</table>
 

The <a href="Http://go.microsoft.com/fwlink/p/?linkid=83936">IPropertyBag</a> interface accepts <i>LPCOLESTR</i> as part of the <a href="Http://go.microsoft.com/fwlink/p/?linkid=83934">IPropertyBag::Read</a> and <a href="Http://go.microsoft.com/fwlink/p/?linkid=83936">IPropertyBag::Write</a> methods. For convenience, the string values for these properties are defined inside <b>netlistmgr.h</b> using the same names.



