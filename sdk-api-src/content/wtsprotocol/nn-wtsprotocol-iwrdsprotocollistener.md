---
UID: NN:wtsprotocol.IWRdsProtocolListener
title: IWRdsProtocolListener
author: windows-sdk-content
description: Exposes methods that request that the protocol start and stop listening for client connection requests.
old-location: termserv\iwrdsprotocollistener.htm
old-project: termserv
ms.assetid: 19d3176a-3f47-46c1-8bee-8e0f1d9b466e
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IWRdsProtocolListener, IWRdsProtocolListener interface [Remote Desktop Services], IWRdsProtocolListener interface [Remote Desktop Services],described, termserv.iwrdsprotocollistener, wtsprotocol/IWRdsProtocolListener
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolListener
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolListener interface


## -description


Exposes methods that request that the protocol start and stop listening for client connection requests. The interface is implemented by the protocol, and its methods are called by the Remote Desktop Services service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolListener</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsProtocolListener</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolListener</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/644eaa8f-776d-49de-af23-de9faef80e74">GetSettings</a>
</td>
<td align="left" width="63%">
Gets the listener setting information for client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3797411-2ac6-4d3c-8c90-5c566e6d8fa8">StartListen</a>
</td>
<td align="left" width="63%">
Notifies the protocol to start listening for client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfb758e8-3d71-47b9-bf7d-075c0c401177">StopListen</a>
</td>
<td align="left" width="63%">
Notifies the protocol to stop listening for client connection requests.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



