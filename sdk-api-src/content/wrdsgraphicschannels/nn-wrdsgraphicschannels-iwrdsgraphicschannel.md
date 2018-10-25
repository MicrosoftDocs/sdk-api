---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannel
title: IWRdsGraphicsChannel
author: windows-sdk-content
description: This interface is used by the RemoteFX graphics services to send and receive data to a virtual graphics channel.
old-location: termserv\iwrdsgraphicschannel.htm
tech.root: termserv
ms.assetid: 5d1e88b4-3dff-4f88-a6de-abc02da57ece
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IWRdsGraphicsChannel, IWRdsGraphicsChannel interface [Remote Desktop Services], IWRdsGraphicsChannel interface [Remote Desktop Services],described, termserv.iwrdsgraphicschannel, wrdsgraphicschannels/IWRdsGraphicsChannel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wrdsgraphicschannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
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
 - wrdsgraphicschannels.h
api_name:
 - IWRdsGraphicsChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsGraphicsChannel interface


## -description


This interface is used by the RemoteFX graphics services to send and receive data to a virtual graphics channel. An instance of this interface is provided to the RemoteFX graphics services in response to the <a href="https://msdn.microsoft.com/2dcce4ac-aa1d-4bdf-9c95-8737f924d0e9">IWRdsGraphicsChannelManager::CreateChannel</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsGraphicsChannel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsGraphicsChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsGraphicsChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e3fb05d-0f5b-4ac3-b121-e6a1662c6ea2">Close</a>
</td>
<td align="left" width="63%">
Called to close the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">Open</a>
</td>
<td align="left" width="63%">
Called to open a channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">Write</a>
</td>
<td align="left" width="63%">
Called to send data to the virtual channel.

</td>
</tr>
</table> 

