---
UID: NN:wsdclient.IWSDServiceProxy
title: IWSDServiceProxy (wsdclient.h)
description: Represents a remote WSD service for client applications and middleware.
helpviewer_keywords: ["IWSDServiceProxy","IWSDServiceProxy interface","IWSDServiceProxy interface","described","ncd.iwsdserviceproxy","wsdclient/IWSDServiceProxy"]
old-location: ncd\iwsdserviceproxy.htm
tech.root: ncd
ms.assetid: 8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxy, IWSDServiceProxy interface, IWSDServiceProxy interface,described, ncd.iwsdserviceproxy, wsdclient/IWSDServiceProxy
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDServiceProxy
 - wsdclient/IWSDServiceProxy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDServiceProxy
---

# IWSDServiceProxy interface


## -description

Represents a remote WSD service for client applications and middleware.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDServiceProxy</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdmetadataexchange">IWSDMetadataExchange</a>. <b>IWSDServiceProxy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDServiceProxy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-begingetmetadata">BeginGetMetadata</a>
</td>
<td align="left" width="63%">
Initiates an asynchronous metadata exchange request with the remote service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-endgetmetadata">EndGetMetadata</a>
</td>
<td align="left" width="63%">
Completes the asynchronous metadata exchange request and retrieves the service metadata from the response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-getendpointproxy">GetEndpointProxy</a>
</td>
<td align="left" width="63%">
Gets the endpoint proxy for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-getservicemetadata">GetServiceMetadata</a>
</td>
<td align="left" width="63%">
Retrieves the metadata for the <b>IWSDServiceProxy</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-seteventingstatuscallback">SetEventingStatusCallback</a>
</td>
<td align="left" width="63%">
Sets or clears the eventing status callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-subscribetooperation">SubscribeToOperation</a>
</td>
<td align="left" width="63%">
Subscribes to a notification or solicit/response event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxy-unsubscribetooperation">UnsubscribeToOperation</a>
</td>
<td align="left" width="63%">
Cancels a subscription to a notification or solicit/response event.

</td>
</tr>
</table>

## -remarks

Service proxy objects may reside on multiple endpoints. An endpoint more completely represents a URL (contains additional useful data). For example, one endpoint may support HTTP on IPv4 addresses and another may support HTTPS on IPv6 addresses. Since the same service lives on both endpoints, it is important that the service have underlying endpoint proxy objects, with each endpoint proxy corresponding to a single endpoint at which the service is available. The endpoint proxy takes care of simple messaging requests to the service, for example, sending one-way or two-way messages.

<b>IWSDServiceProxy</b> objects are employed to obtain service metadata, send messages to the service through a service proxy, subscribe to events on the service, and bind to proxies that provide type-specific semantics.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdmetadataexchange">IWSDMetadataExchange</a>

