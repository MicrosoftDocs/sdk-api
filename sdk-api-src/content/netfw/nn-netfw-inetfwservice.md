---
UID: NN:netfw.INetFwService
title: INetFwService
author: windows-sdk-content
description: The INetFwService interface provides access to the properties of a service that may be authorized to listen through the firewall.
old-location: ics\inetfwservice.htm
tech.root: ICS
ms.assetid: 57a777a4-03f5-416a-ae28-474d8794a759
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: INetFwService, INetFwService interface [ICS/ICF], INetFwService interface [ICS/ICF],described, ics.inetfwservice, netfw/INetFwService
ms.prod: windows
ms.technology: windows-sdk
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
 - INetFwService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwService interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwService</b> interface provides access to the properties of a service that may be authorized to
listen through the firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwService</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INetFwService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c26863a-b0eb-4e5a-b3a9-0129ab9a4df2">get_Customized</a>
</td>
<td align="left" width="63%">
Gets the flag showing whether at least one of the ports associated with the service
   has been customized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf690427-ad2e-4a5b-9651-f6a9382ab341">get_Enabled</a>
</td>
<td align="left" width="63%">
Gets the flag showing if all the ports associated with the service are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51f0440f-6e0c-48b2-9dc0-bec503192fa1">get_GloballyOpenPorts</a>
</td>
<td align="left" width="63%">
Gets the collection of globally open ports associated with the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/992f39f6-ffb7-40c0-9227-6e626f226313">get_IpVersion</a>
</td>
<td align="left" width="63%">
Gets the IP version for which the service is authorized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b6179d0-c16d-43f7-8575-b173841cffe9">get_Name</a>
</td>
<td align="left" width="63%">
Gets the friendly name of the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">get_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Gets the contents of the RemoteAddress property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5bd787f-e00c-4a57-adc7-a9618809198a">get_Scope</a>
</td>
<td align="left" width="63%">
Gets the contents of the Scope property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22f91e9a-e5b2-47a1-8ccb-b033c7d88286">get_Type</a>
</td>
<td align="left" width="63%">
Gets the type of the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf690427-ad2e-4a5b-9651-f6a9382ab341">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets the flag showing if all the ports associated with the service are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/992f39f6-ffb7-40c0-9227-6e626f226313">put_IpVersion</a>
</td>
<td align="left" width="63%">
Sets the IP version for which the service is authorized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">put_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Sets the contents of the RemoteAddress property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5bd787f-e00c-4a57-adc7-a9618809198a">put_Scope</a>
</td>
<td align="left" width="63%">
Sets the contents of the Scope property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwService</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6c26863a-b0eb-4e5a-b3a9-0129ab9a4df2">Customized</a>


</td>
<td align="left" width="63%">
Accesses the flag showing whether at least one of the ports associated with the service
   has been customized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bf690427-ad2e-4a5b-9651-f6a9382ab341">Enabled</a>


</td>
<td align="left" width="63%">
Accesses the flag showing if all the ports associated with the service are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/51f0440f-6e0c-48b2-9dc0-bec503192fa1">GloballyOpenPorts</a>


</td>
<td align="left" width="63%">
Accesses the collection of open ports associated with the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3b6179d0-c16d-43f7-8575-b173841cffe9">Name</a>


</td>
<td align="left" width="63%">
Read-only access to the name of the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5c38a9fc-b7d9-436d-92e6-8b0aec5e8628">RemoteAddresses</a>


</td>
<td align="left" width="63%">
Accesses the RemoteAddress property for this port.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a5bd787f-e00c-4a57-adc7-a9618809198a">Scope</a>


</td>
<td align="left" width="63%">
Accesses the   Scope property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/22f91e9a-e5b2-47a1-8ccb-b033c7d88286">Type</a>


</td>
<td align="left" width="63%">
Read-only access to the type of the service.

</td>
</tr>
</table> 


## -remarks



Instances of this interface are retrieved
through the <a href="https://msdn.microsoft.com/b99464c5-dabc-405a-ad3e-da06a6faef47">INetFwServices</a> collection. 

All configuration changes take
effect immediately.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/b99464c5-dabc-405a-ad3e-da06a6faef47">INetFwServices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

