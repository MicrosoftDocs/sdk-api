---
UID: NN:wtsprotocol.IWRdsProtocolManager
title: IWRdsProtocolManager
author: windows-sdk-content
description: Exposes methods that the Remote Desktop Services service uses to communicate with the protocol provider.
old-location: termserv\iwrdsprotocolmanager.htm
tech.root: TermServ
ms.assetid: 626d579a-88a2-4f72-9d91-b27e517b4806
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolManager, IWRdsProtocolManager interface [Remote Desktop Services], IWRdsProtocolManager interface [Remote Desktop Services],described, termserv.iwrdsprotocolmanager, wtsprotocol/IWRdsProtocolManager
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
 - IWRdsProtocolManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolManager interface


## -description


Exposes methods that  the Remote Desktop Services service uses to communicate with the protocol provider. It is the only interface in the protocol provider for which the Remote Desktop Services service calls <a href="https://msdn.microsoft.com/3b414b95-e8d2-42e8-b4f2-5cc5189a3d08">CoCreateInstanceEx</a>. In addition, the first call the Remote Desktop Services service makes into the protocol provider is to the <a href="https://msdn.microsoft.com/df91dc10-77af-4b5a-8033-1b1ff614bb17">CreateListener</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsProtocolManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df91dc10-77af-4b5a-8033-1b1ff614bb17">CreateListener</a>
</td>
<td align="left" width="63%">
Requests the creation of an <a href="https://msdn.microsoft.com/19d3176a-3f47-46c1-8bee-8e0f1d9b466e">IWRdsProtocolListener</a> object that listens for incoming client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c63c794c-41a0-4f07-be93-ba24dc156ca2">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the protocol manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32b2a05a-d5de-4f2f-bcaa-587cf22aa5c5">NotifyServiceStateChange</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the state of the Remote Desktop Services service is changing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0beb07a-69a0-4cb8-adcb-f95d8fd721df">NotifySessionOfServiceStart</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the Remote Desktop Services service has started for a given session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acf52eb0-d8f8-4257-9c2c-e9345c0f1b7f">NotifySessionOfServiceStop</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72438718-1a66-473b-a563-67cfc8095318">NotifySessionStateChange</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider of changes in the state of a session. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80292d9b-fced-4726-8f83-5ba355df06a2">NotifySettingsChange</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider of changes in the settings within the Remote Desktop Services service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d7bc6e3-798e-4dc8-8892-7be6992b67ab">Uninitialize</a>
</td>
<td align="left" width="63%">
Uninitializes the protocol manager.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



