---
UID: NN:netcon.INetSharingConfiguration
title: INetSharingConfiguration
author: windows-sdk-content
description: The INetSharingConfiguration interface provides methods to manage connection sharing, port mapping, and Internet Connection Firewall.
old-location: ics\inetsharingconfiguration.htm
old-project: ICS
ms.assetid: 3ed1a3ae-87af-4415-b149-c66ae65cd053
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: INetSharingConfiguration, INetSharingConfiguration interface [ICS/ICF], INetSharingConfiguration interface [ICS/ICF],described, _ics_inetsharingconfiguration, ics.inetsharingconfiguration, netcon/INetSharingConfiguration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: SHARINGCONNECTIONTYPE, *LPSHARINGCONNECTIONTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingConfiguration
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetSharingConfiguration interface


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>INetSharingConfiguration</b> interface provides methods to manage connection sharing, port mapping, and Internet Connection Firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetSharingConfiguration</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetSharingConfiguration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INetSharingConfiguration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d9e1520-6018-425c-a2f9-c408fa3025cf">AddPortMapping</a>
</td>
<td align="left" width="63%">
Adds a service-port mapping for this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0157376-7533-4155-801c-3db82290655d">DisableInternetFirewall</a>
</td>
<td align="left" width="63%">
Disables Internet Connection Firewall on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85fda578-603c-4447-8546-374077235943">DisableSharing</a>
</td>
<td align="left" width="63%">
Disables sharing on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9805f6bf-ee06-469f-9b2f-e48caa582d1a">EnableInternetFirewall</a>
</td>
<td align="left" width="63%">
Enables Internet Connection Firewall on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40b2a2ff-50f4-484c-bf79-ae99a348644f">EnableSharing</a>
</td>
<td align="left" width="63%">
Enables sharing on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5465acc-2b36-47d1-b48f-b36df3a8efb3">EnumPortMappings</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/68334bd2-353f-457d-a2c7-1271816f10f5">IEnumNetSharingPortMapping</a> interface for this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85f6b76f-3c31-4669-a54f-30d12a82935e">get_InternetFirewallEnabled</a>
</td>
<td align="left" width="63%">
Determines whether Internet Connection Firewall is enabled on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29dfc1cf-4b72-4ba8-9a5c-7e7dd20393ee">get_SharingConnectionType</a>
</td>
<td align="left" width="63%">
Determines the type of sharing on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8872235-0ef3-4ade-8085-fd90f40549af">get_SharingEnabled</a>
</td>
<td align="left" width="63%">
Determines whether sharing is enabled on this connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2790aced-a3a9-425d-9e0f-fe8df4fcb934">RemovePortMapping</a>
</td>
<td align="left" width="63%">
Removes a service-port mapping for this connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8f774509-0efb-49e5-bf56-61f4810631bd">INetSharingManager::get_INetSharingConfigurationForINetConnection</a>



<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

