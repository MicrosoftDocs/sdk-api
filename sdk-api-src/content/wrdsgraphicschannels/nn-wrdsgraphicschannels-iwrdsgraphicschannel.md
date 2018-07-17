---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannel
title: IWRdsGraphicsChannel
author: windows-sdk-content
description: This interface is used by the RemoteFX graphics services to send and receive data to a virtual graphics channel.
old-location: termserv\iwrdsgraphicschannel.htm
old-project: termserv
ms.assetid: 5d1e88b4-3dff-4f88-a6de-abc02da57ece
ms.author: windowssdkdev
ms.date: 07/10/2018
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
tech.root: 
req.typenames: WRdsGraphicsChannelType
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Called to close the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Called to open a channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439706">Write</a>
</td>
<td align="left" width="63%">
Called to send data to the virtual channel.

</td>
</tr>
</table> 

