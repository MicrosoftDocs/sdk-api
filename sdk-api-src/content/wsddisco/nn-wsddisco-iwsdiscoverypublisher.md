---
UID: NN:wsddisco.IWSDiscoveryPublisher
title: IWSDiscoveryPublisher
author: windows-sdk-content
description: Provides methods for announcing hosts and managing incoming queries to hosts.
old-location: ncd\iwsdiscoverypublisher.htm
old-project: WsdApi
ms.assetid: 4fff1328-d315-4a26-b7d8-43a273133e08
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSDiscoveryPublisher, IWSDiscoveryPublisher interface, IWSDiscoveryPublisher interface,described, ncd.iwsdiscoverypublisher, wsddisco/IWSDiscoveryPublisher
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisher
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryPublisher interface


## -description


Provides methods for announcing hosts and managing incoming queries to hosts.

To get this interface, call <a href="https://msdn.microsoft.com/18abde49-2ea7-4c49-9afe-1b7c7182aeeb">WSDCreateDiscoveryPublisher</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveryPublisher</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDiscoveryPublisher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDiscoveryPublisher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b849b17-0597-4e78-88c6-8ee95bcb754c">GetXMLContext</a>
</td>
<td align="left" width="63%">
Gets the  XML context associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/657f50ad-128f-4ccb-b89a-ed88f5d9b381">MatchProbe</a>
</td>
<td align="left" width="63%">
Determines if a <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> message matches the specified host and sends a <a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatch</a> if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2441bdc-848b-48c4-bc4e-5b8f854cc4a5">MatchProbeEx</a>
</td>
<td align="left" width="63%">
Determines whether a <a href="https://msdn.microsoft.com/a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7">Probe</a> message matches the specified host and sends a <a href="https://msdn.microsoft.com/58d3d016-ae29-4090-9b88-e1125db59c95">ProbeMatch</a> with extended information if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f01a17ce-2a87-4f11-81d3-a94743b309ab">MatchResolve</a>
</td>
<td align="left" width="63%">
Determines if a <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve</a> message matches the specified host and sends a <a href="https://msdn.microsoft.com/0eaa4348-968e-4b45-9509-8b15476edaa1">ResolveMatch</a> if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0eba744c-c335-4b82-95f0-6142cfedad09">MatchResolveEx</a>
</td>
<td align="left" width="63%">
Determines whether a <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve</a> message matches the specified host and sends a <a href="https://msdn.microsoft.com/0eaa4348-968e-4b45-9509-8b15476edaa1">ResolveMatch</a> with extended information if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71c6e4af-128a-4418-9c3b-f64aa734fb50">Publish</a>
</td>
<td align="left" width="63%">
Announces the presence of a network host by sending a <a href="https://msdn.microsoft.com/a7402e02-9bdc-49ec-ba93-8a32f55b9dd8">Hello</a> message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4a1f93d-071b-4244-b4e4-ed7e7bb7432b">PublishEx</a>
</td>
<td align="left" width="63%">
Announces the presence of a network host by sending a <a href="https://msdn.microsoft.com/a7402e02-9bdc-49ec-ba93-8a32f55b9dd8">Hello</a> message with extended information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75a6c593-298b-45b4-bde5-2a383b7581cc">RegisterNotificationSink</a>
</td>
<td align="left" width="63%">
Attaches a callback notification sink to the discovery publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ceb55de-c8be-43a7-93d7-8f674f9645ef">RegisterScopeMatchingRule</a>
</td>
<td align="left" width="63%">
Adds support for a custom scope matching rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01d16205-ca4c-44bb-865c-7fc9fb1db2e1">SetAddressFamily</a>
</td>
<td align="left" width="63%">
Specifies the IP address family (IPv4, IPv6, or both) over which the host will be published.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef403d31-769c-499b-a199-089100725ef9">UnPublish</a>
</td>
<td align="left" width="63%">
Announces the departure of a network host by sending a <a href="https://msdn.microsoft.com/7b9abfcc-28ab-4f29-af69-6dc68e3f51b6">Bye</a> message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaf6bc07-8ce9-41f7-b468-971b31b51a86">UnRegisterNotificationSink</a>
</td>
<td align="left" width="63%">
Detaches a callback notification sink from the discovery publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82af2ea1-8415-45f7-ab05-805a66689482">UnRegisterScopeMatchingRule</a>
</td>
<td align="left" width="63%">
Removes support for a custom scope matching rule.

</td>
</tr>
</table> 


## -remarks



 This interface represents the "server" or "host" side of <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery</a>.




## -see-also




<a href="https://msdn.microsoft.com/2b23d7d3-3b06-48c8-993e-49c72b139624">Overview of the WSDAPI Interfaces</a>
 

 

