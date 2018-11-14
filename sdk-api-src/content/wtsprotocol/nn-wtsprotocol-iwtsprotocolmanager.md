---
UID: NN:wtsprotocol.IWTSProtocolManager
title: IWTSProtocolManager
author: windows-sdk-content
description: IWTSProtocolManager is no longer available. Instead, use IWRdsProtocolManager.
old-location: termserv\iwtsprotocolmanager.htm
tech.root: termserv
ms.assetid: a54bdb46-b18b-4a6d-90fc-75947f6dd191
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWTSProtocolManager, IWTSProtocolManager interface [Remote Desktop Services], IWTSProtocolManager interface [Remote Desktop Services],described, termserv.iwtsprotocolmanager, wtsprotocol/IWTSProtocolManager
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWTSProtocolManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolManager interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolManager</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a>.]

Exposes methods that  the Remote Desktop Services service uses to communicate with the protocol provider. It is the only interface in the protocol provider for which the Remote Desktop Services service calls <a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>. In addition, the first call the Remote Desktop Services service makes into the protocol provider is to the <a href="https://msdn.microsoft.com/2c947181-5cac-40c1-b993-537b580efafe">CreateListener</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSProtocolManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c947181-5cac-40c1-b993-537b580efafe">CreateListener</a>
</td>
<td align="left" width="63%">
Requests the creation of an <a href="https://msdn.microsoft.com/b11eb19f-ffc3-4a68-85c6-90a2412168f8">IWTSProtocolListener</a> object that listens for incoming client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/303a53b3-b297-486c-9422-706ec60441f2">NotifyServiceStateChange</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the state of the Remote Desktop Services service is changing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b9e7578-75e1-4447-8ff9-e391bf339fbe">NotifySessionOfServiceStart</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the Remote Desktop Services service has started for a given session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdad7006-4cd5-4ea3-84a3-f3cdeb57befa">NotifySessionOfServiceStop</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59c284bf-8175-46d2-ab44-8b2975574c14">NotifySessionStateChange</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider of changes in the state of a session. 

</td>
</tr>
</table> 

