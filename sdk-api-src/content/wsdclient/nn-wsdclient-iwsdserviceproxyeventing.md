---
UID: NN:wsdclient.IWSDServiceProxyEventing
title: IWSDServiceProxyEventing
author: windows-sdk-content
description: Represents a remote WSD service for client applications and middleware. This interface allows for the implementation of multiple asynchronous operations.
old-location: ncd\iwsdserviceproxyeventing.htm
tech.root: WsdApi
ms.assetid: c9454636-6d6a-4344-a954-1bd35195aff9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDServiceProxyEventing, IWSDServiceProxyEventing interface, IWSDServiceProxyEventing interface,described, ncd.iwsdserviceproxyeventing, wsdclient/IWSDServiceProxyEventing
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDServiceProxyEventing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/cf42f680-f19c-4ee3-824d-dc892608d4d2">BeginGetStatusForMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that retrieves the current status for a collection of event subscriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac93a29a-789f-4aa0-b804-b4d0a5b89ee2">BeginRenewMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54c6ac58-4272-45ad-80cc-2114ba6f466e">BeginSubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8a3dd48-89a2-4d7b-98e0-3dcb3c32cb2b">BeginUnsubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an  asynchronous cancellation request for a subscription to  a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0918ef4f-29ae-4c74-9b7d-0e7adb514c7b">EndGetStatusForMultipleOperations</a>
</td>
<td align="left" width="63%">
Initializes an asynchronous operation that retrieves the current status for a collection of event subscriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb5be204-a775-4abb-af5b-9a829b69fa14">EndRenewMultipleOperations</a>
</td>
<td align="left" width="63%">
Completes an asynchronous operation that renews a collection of existing notification subscriptions by submitting a new duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e3cdb10-fde9-4936-9a7d-61404a754faa">EndSubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Completes an asynchronous operation that subscribes to a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62f42441-11b0-46ce-9a4e-03b34d8b4c9b">EndUnsubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Completes an  asynchronous cancellation request for a subscription to  a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba9c6d6e-d551-4010-b3b7-9e5391de9c49">GetStatusForMultipleOperations</a>
</td>
<td align="left" width="63%">
Retrieves the current status for a collection of event subscriptions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67c5fa63-3512-4b03-afb4-9b97b26200aa">RenewMultipleOperations</a>
</td>
<td align="left" width="63%">
Renews a collection of existing notification subscriptions by submitting a new duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0df5b429-5b6e-4cef-af05-7f615c93aa0f">SubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Subscribes to a collection of notifications or solicit/response events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f542dc1-639c-4201-9274-8aa5cc238482">UnsubscribeToMultipleOperations</a>
</td>
<td align="left" width="63%">
Cancels a collection of subscriptions to notifications or solicit/request events.

</td>
</tr>
</table> 

