---
UID: NN:wsddisco.IWSDiscoveryPublisher
title: IWSDiscoveryPublisher (wsddisco.h)
author: windows-sdk-content
description: Provides methods for announcing hosts and managing incoming queries to hosts.
old-location: ncd\iwsdiscoverypublisher.htm
tech.root: WsdApi
ms.assetid: 4fff1328-d315-4a26-b7d8-43a273133e08
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher, IWSDiscoveryPublisher interface, IWSDiscoveryPublisher interface,described, ncd.iwsdiscoverypublisher, wsddisco/IWSDiscoveryPublisher
ms.topic: interface
f1_keywords: 
 - "wsddisco/IWSDiscoveryPublisher"
dev_langs:
 - c++
req.header: wsddisco.h
req.include-header: Wsdapi.h
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryPublisher
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDiscoveryPublisher interface


## -description


Provides methods for announcing hosts and managing incoming queries to hosts.

To get this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-wsdcreatediscoverypublisher">WSDCreateDiscoveryPublisher</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDiscoveryPublisher</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDiscoveryPublisher</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-getxmlcontext">GetXMLContext</a>
</td>
<td align="left" width="63%">
Gets the  XML context associated with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchprobe">MatchProbe</a>
</td>
<td align="left" width="63%">
Determines if a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/probe-message">Probe</a> message matches the specified host and sends a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/probematches-message">ProbeMatch</a> if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchprobeex">MatchProbeEx</a>
</td>
<td align="left" width="63%">
Determines whether a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/probe-message">Probe</a> message matches the specified host and sends a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/probematches-message">ProbeMatch</a> with extended information if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchresolve">MatchResolve</a>
</td>
<td align="left" width="63%">
Determines if a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolve-message">Resolve</a> message matches the specified host and sends a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolvematches-message">ResolveMatch</a> if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-matchresolveex">MatchResolveEx</a>
</td>
<td align="left" width="63%">
Determines whether a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolve-message">Resolve</a> message matches the specified host and sends a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/resolvematches-message">ResolveMatch</a> with extended information if the match is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-publish">Publish</a>
</td>
<td align="left" width="63%">
Announces the presence of a network host by sending a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/hello-message">Hello</a> message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-publishex">PublishEx</a>
</td>
<td align="left" width="63%">
Announces the presence of a network host by sending a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/hello-message">Hello</a> message with extended information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-registernotificationsink">RegisterNotificationSink</a>
</td>
<td align="left" width="63%">
Attaches a callback notification sink to the discovery publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-registerscopematchingrule">RegisterScopeMatchingRule</a>
</td>
<td align="left" width="63%">
Adds support for a custom scope matching rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-setaddressfamily">SetAddressFamily</a>
</td>
<td align="left" width="63%">
Specifies the IP address family (IPv4, IPv6, or both) over which the host will be published.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-unpublish">UnPublish</a>
</td>
<td align="left" width="63%">
Announces the departure of a network host by sending a <a href="https://docs.microsoft.com/windows/desktop/WsdApi/bye-message">Bye</a> message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-unregisternotificationsink">UnRegisterNotificationSink</a>
</td>
<td align="left" width="63%">
Detaches a callback notification sink from the discovery publisher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoverypublisher-unregisterscopematchingrule">UnRegisterScopeMatchingRule</a>
</td>
<td align="left" width="63%">
Removes support for a custom scope matching rule.

</td>
</tr>
</table> 


## -remarks



 This interface represents the "server" or "host" side of <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WsdApi/overview-of-the-wsdapi-interfaces">Overview of the WSDAPI Interfaces</a>
 

 

