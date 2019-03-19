---
UID: NN:wsdclient.IWSDServiceProxy
title: IWSDServiceProxy (wsdclient.h)
author: windows-sdk-content
description: Represents a remote WSD service for client applications and middleware.
old-location: ncd\iwsdserviceproxy.htm
tech.root: WsdApi
ms.assetid: 8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDServiceProxy, IWSDServiceProxy interface, IWSDServiceProxy interface,described, ncd.iwsdserviceproxy, wsdclient/IWSDServiceProxy
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDServiceProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceProxy interface


## -description


Represents a remote WSD service for client applications and middleware.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDServiceProxy</b> interface inherits from <a href="https://msdn.microsoft.com/f4e2c2f7-3e76-4a17-88f8-9d59c18343a9">IWSDMetadataExchange</a>. <b>IWSDServiceProxy</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/bcc0bcaf-76fb-4dca-b946-2826809a53a1">BeginGetMetadata</a>
</td>
<td align="left" width="63%">
Initiates an asynchronous metadata exchange request with the remote service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6024770a-e4cb-4db1-9767-51b559fd8244">EndGetMetadata</a>
</td>
<td align="left" width="63%">
Completes the asynchronous metadata exchange request and retrieves the service metadata from the response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c236f31-e3ba-4678-a4fe-1e078c9f9af3">GetEndpointProxy</a>
</td>
<td align="left" width="63%">
Gets the endpoint proxy for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/552da68f-6e6a-44b2-8c95-e29bc67de3c2">GetServiceMetadata</a>
</td>
<td align="left" width="63%">
Retrieves the metadata for the <b>IWSDServiceProxy</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a924df4-93a7-4443-a384-0a89d5d90509">SetEventingStatusCallback</a>
</td>
<td align="left" width="63%">
Sets or clears the eventing status callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3294bd7-f3df-4571-92f6-eb6bc57240fb">SubscribeToOperation</a>
</td>
<td align="left" width="63%">
Subscribes to a notification or solicit/response event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b306239c-95a4-4a1d-990c-193237bad275">UnsubscribeToOperation</a>
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




<a href="https://msdn.microsoft.com/f4e2c2f7-3e76-4a17-88f8-9d59c18343a9">IWSDMetadataExchange</a>
 

 

