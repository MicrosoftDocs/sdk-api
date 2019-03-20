---
UID: NN:wtsprotocol.IWRdsProtocolShadowConnection
title: IWRdsProtocolShadowConnection (wtsprotocol.h)
author: windows-sdk-content
description: Exposes methods that notify the protocol provider about the status of session shadowing.
old-location: termserv\iwrdsprotocolshadowconnection.htm
tech.root: TermServ
ms.assetid: d23c4902-4e61-45ff-8a49-62eea1b92d4a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolShadowConnection, IWRdsProtocolShadowConnection interface [Remote Desktop Services], IWRdsProtocolShadowConnection interface [Remote Desktop Services],described, termserv.iwrdsprotocolshadowconnection, wtsprotocol/IWRdsProtocolShadowConnection
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
 - IWRdsProtocolShadowConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolShadowConnection interface


## -description


Exposes methods that notify the protocol provider about the status of session shadowing. The <b>IWRdsProtocolShadowConnection</b> interface can also be used to exchange information between the shadow client and the shadow target. This interface is implemented by the protocol provider, and its methods are called by the Remote Desktop Services service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolShadowConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsProtocolShadowConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolShadowConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fe2e3fb-f368-4b7e-b679-402db900916c">DoTarget</a>
</td>
<td align="left" width="63%">
Requests that the protocol start the target side of a shadow connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f7b5811-6aba-41f2-9fa4-2bbc4c6e005c">Start</a>
</td>
<td align="left" width="63%">
Notifies the protocol that shadowing has started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6abe698-a390-485a-9a31-823ff25351c2">Stop</a>
</td>
<td align="left" width="63%">
Notifies the protocol that shadowing has stopped.

</td>
</tr>
</table> 

