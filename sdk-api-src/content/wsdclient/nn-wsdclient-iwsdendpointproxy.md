---
UID: NN:wsdclient.IWSDEndpointProxy
title: IWSDEndpointProxy
author: windows-sdk-content
description: Implements a device services messaging proxy.
old-location: ncd\iwsdendpointproxy.htm
tech.root: WsdApi
ms.assetid: 58ca085f-8939-413c-8fd3-4d867b1cf490
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWSDEndpointProxy, IWSDEndpointProxy interface, IWSDEndpointProxy interface,described, ncd.iwsdendpointproxy, wsdclient/IWSDEndpointProxy
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWSDEndpointProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDEndpointProxy interface


## -description


Implements a device services messaging proxy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDEndpointProxy</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDEndpointProxy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDEndpointProxy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/559c7fcd-9652-4dfa-b22a-45929b6aee14">AbortAsyncOperation</a>
</td>
<td align="left" width="63%">
Aborts a pending asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/950f5634-1cc5-4981-9053-e9090374cc5e">GetErrorInfo</a>
</td>
<td align="left" width="63%">
Retrieves information on the last error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45ed30fd-7e4f-44f5-bb90-5686746e39be">GetFaultInfo</a>
</td>
<td align="left" width="63%">
Retrieves information on the last received fault.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f63c8c7c-8581-49d4-a29d-a7b0b46a2db5">ProcessFault</a>
</td>
<td align="left" width="63%">
Processes the fault information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e610c68f-1fce-42fa-8527-8ca2d9267c90">SendOneWayRequest</a>
</td>
<td align="left" width="63%">
Sends a one-way request message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f93ddbf1-d530-4957-87ab-5718ee5f20d9">SendTwoWayRequest</a>
</td>
<td align="left" width="63%">
Sends a two-way request message using a synchronous call pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf175e79-9df2-4481-b784-e2cc40e34222">SendTwoWayRequestAsync</a>
</td>
<td align="left" width="63%">
Sends a two-way request message using an asynchronous call pattern.

</td>
</tr>
</table> 


## -remarks



Service proxy objects may reside on multiple endpoints. An endpoint more completely represents a URL (contains additional useful data). One endpoint may support HTTP on IPv4 addresses and another may support HTTPS on IPv6 addresses. Since the same service lives on both endpoints, it is important that the service have underlying endpoint proxy objects, with each endpoint proxy corresponding to a single endpoint at which the service is available. The endpoint proxy takes care of simple messaging requests to the service, for example, sending one-way or two-way messages.

Endpoint proxies are generally used inside WSDAPI, but they can be retrieved from <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> or <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> objects to expose message-level functionality.



