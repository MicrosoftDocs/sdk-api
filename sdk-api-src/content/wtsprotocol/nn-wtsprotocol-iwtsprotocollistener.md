---
UID: NN:wtsprotocol.IWTSProtocolListener
title: IWTSProtocolListener
author: windows-sdk-content
description: IWTSProtocolListener is no longer available. Instead, use IWRdsProtocolListener.
old-location: termserv\iwtsprotocollistener.htm
tech.root: termserv
ms.assetid: b11eb19f-ffc3-4a68-85c6-90a2412168f8
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IWTSProtocolListener, IWTSProtocolListener interface [Remote Desktop Services], IWTSProtocolListener interface [Remote Desktop Services],described, termserv.iwtsprotocollistener, wtsprotocol/IWTSProtocolListener
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWTSProtocolListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolListener interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolListener</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a>.]

Exposes methods that request that the protocol start and stop listening for client connection requests. The interface is implemented by the protocol and its methods are called by the Remote Desktop Services service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolListener</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSProtocolListener</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolListener</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d922ea90-a4eb-4495-947c-ef33bd81f40a">StartListen</a>
</td>
<td align="left" width="63%">
Notifies the protocol to start listening for client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c5b09d3-74d6-4067-b18b-ed2a54af4153">StopListen</a>
</td>
<td align="left" width="63%">
Notifies the protocol to stop listening for client connection requests.

</td>
</tr>
</table> 

