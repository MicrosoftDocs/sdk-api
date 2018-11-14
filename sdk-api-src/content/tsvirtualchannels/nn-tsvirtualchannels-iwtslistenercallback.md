---
UID: NN:tsvirtualchannels.IWTSListenerCallback
title: IWTSListenerCallback
author: windows-sdk-content
description: Used to notify the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.
old-location: termserv\iwtslistenercallback.htm
tech.root: termserv
ms.assetid: b5f1d74d-31e6-4447-82ab-6dd3ad9957fd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWTSListenerCallback, IWTSListenerCallback interface [Remote Desktop Services], IWTSListenerCallback interface [Remote Desktop Services],described, termserv.iwtslistenercallback, tsvirtualchannels/IWTSListenerCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
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
 - TsVirtualChannels.h
api_name:
 - IWTSListenerCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

