---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWTSListenerCallback interface


## -description


Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests  on a particular listener.

This interface is implemented by the Remote Desktop Connection (RDC) client plug-in. Calls will always be made on the same thread, with the exception of an out-of-process plug-in, where the calls will arrive on a remote procedure call (RPC) thread pool.
Implementation should not block these calls because this may block other incoming connections or data on existing connections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSListenerCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSListenerCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSListenerCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fa2b063-3a41-4f56-8cc1-8a829e530fb2">OnNewChannelConnection</a>
</td>
<td align="left" width="63%">
Allows the RDC client plug-in to accept or deny a connection request for an incoming connection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ecc673ec-1bea-4e7c-b1b5-a2342445f6cf">DVC Client Plug-in Example</a>
 

 

