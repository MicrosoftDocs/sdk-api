---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannelEvents
title: IWRdsGraphicsChannelEvents
author: windows-sdk-content
description: This interface receives notifications that relate to a graphics virtual channel.
old-location: termserv\iwrdsgraphicschannelevents.htm
tech.root: TermServ
ms.assetid: 59802a2d-bdb0-4792-b667-5095d4a02b06
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsGraphicsChannelEvents, IWRdsGraphicsChannelEvents interface [Remote Desktop Services], IWRdsGraphicsChannelEvents interface [Remote Desktop Services],described, termserv.iwrdsgraphicschannelevents, wrdsgraphicschannels/IWRdsGraphicsChannelEvents
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWRdsGraphicsChannelEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsGraphicsChannelEvents interface


## -description


This interface receives notifications that relate to a graphics virtual channel. This interface is implemented by the RemoteFX graphics services and a pointer to this interface is provided to the graphics virtual channel in the <a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsGraphicsChannelEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsGraphicsChannelEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsGraphicsChannelEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dafff806-8b63-40cd-8b04-efb0497cb043">OnChannelOpened</a>
</td>
<td align="left" width="63%">
Called when the channel has been opened and is ready for use, or when an error occurs when a channel is opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd195c0e-68bf-4361-9795-0e436c1abc90">OnClose</a>
</td>
<td align="left" width="63%">
Called when the channel has been closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac202fa0-6277-440a-8292-a785bbc78730">OnDataReceived</a>
</td>
<td align="left" width="63%">
Called when a full message is received from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb5af337-a412-4bda-862f-7e12705d0446">OnDataSent</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://msdn.microsoft.com/6ce627d8-078d-427a-b732-473d4f44f719">IWRdsGraphicsChannel::Write</a> method is called and the data has been sent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d955041a-6179-4bf2-9a1b-766f459f3776">OnMetricsUpdate</a>
</td>
<td align="left" width="63%">
Called to notify the RemoteFX graphics services that network conditions have changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3b32b37f-6b1f-4682-9e2e-4a64e5c36e04">IWRdsGraphicsChannel::Open</a>
 

 

