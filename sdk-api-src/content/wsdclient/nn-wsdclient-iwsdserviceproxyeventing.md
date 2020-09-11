---
UID: NN:wsdclient.IWSDServiceProxyEventing
title: IWSDServiceProxyEventing (wsdclient.h)
description: Represents a remote WSD service for client applications and middleware. This interface allows for the implementation of multiple asynchronous operations.
helpviewer_keywords: ["IWSDServiceProxyEventing","IWSDServiceProxyEventing interface","IWSDServiceProxyEventing interface","described","ncd.iwsdserviceproxyeventing","wsdclient/IWSDServiceProxyEventing"]
old-location: ncd\iwsdserviceproxyeventing.htm
tech.root: ncd
ms.assetid: c9454636-6d6a-4344-a954-1bd35195aff9
ms.date: 12/05/2018
ms.keywords: IWSDServiceProxyEventing, IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,described, ncd.iwsdserviceproxyeventing, wsdclient/IWSDServiceProxyEventing
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdclient.idl
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
 - IWSDServiceProxyEventing
 - wsdclient/IWSDServiceProxyEventing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDServiceProxyEventing
---

# IWSDServiceProxyEventing interface


## -description

Represents a remote WSD service for client applications and middleware.  This interface allows for the implementation of multiple asynchronous operations.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDServiceProxyEventing</b> interface inherits from <b>IWSDServiceProxy</b>. <b>IWSDServiceProxyEventing</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDServiceProxyEventing</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-begingetstatusformultipleoperations">BeginGetStatusForMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that retrieves the current status for a collection of event subscriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-beginrenewmultipleoperations">BeginRenewMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-beginsubscribetomultipleoperations">BeginSubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-beginunsubscribetomultipleoperations">BeginUnsubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an  asynchronous cancellation request for a subscription to  a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-endgetstatusformultipleoperations">EndGetStatusForMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that retrieves the current status for a collection of event subscriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-endrenewmultipleoperations">EndRenewMultipleOperations</a>
</td>
<td align="left" width="63%">
Completes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-endsubscribetomultipleoperations">EndSubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Completes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-endunsubscribetomultipleoperations">EndUnsubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Completes an  asynchronous cancellation request for a subscription to  a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-getstatusformultipleoperations">GetStatusForMultipleOperations</a>
</td>
<td align="left" width="63%">
Retrieves the current status for a collection of event subscriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-renewmultipleoperations">RenewMultipleOperations</a>
</td>
<td align="left" width="63%">
Renews a collection of existing notification subscriptions by submitting a new duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-subscribetomultipleoperations">SubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Subscribes to a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdserviceproxyeventing-unsubscribetomultipleoperations">UnsubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Cancels a collection of subscriptions to notifications or solicit/request events.

</td>
</tr>
</table>

