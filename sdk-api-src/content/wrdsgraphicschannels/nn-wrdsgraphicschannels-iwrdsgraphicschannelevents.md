---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannelEvents
title: IWRdsGraphicsChannelEvents (wrdsgraphicschannels.h)
author: windows-sdk-content
description: This interface receives notifications that relate to a graphics virtual channel.
old-location: termserv\iwrdsgraphicschannelevents.htm
tech.root: TermServ
ms.assetid: 59802a2d-bdb0-4792-b667-5095d4a02b06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannelEvents, IWRdsGraphicsChannelEvents interface [Remote Desktop Services], IWRdsGraphicsChannelEvents interface [Remote Desktop Services],described, termserv.iwrdsgraphicschannelevents, wrdsgraphicschannels/IWRdsGraphicsChannelEvents
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
ms.custom: 19H1
---

# IWRdsGraphicsChannelEvents interface


## -description


This interface receives notifications that relate to a graphics virtual channel. This interface is implemented by the RemoteFX graphics services and a pointer to this interface is provided to the graphics virtual channel in the <a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">IWRdsGraphicsChannel::Open</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsGraphicsChannelEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsGraphicsChannelEvents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onchannelopened">OnChannelOpened</a>
</td>
<td align="left" width="63%">
Called when the channel has been opened and is ready for use, or when an error occurs when a channel is opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onclose">OnClose</a>
</td>
<td align="left" width="63%">
Called when the channel has been closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-ondatareceived">OnDataReceived</a>
</td>
<td align="left" width="63%">
Called when a full message is received from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-ondatasent">OnDataSent</a>
</td>
<td align="left" width="63%">
Called when the <a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-write">IWRdsGraphicsChannel::Write</a> method is called and the data has been sent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelevents-onmetricsupdate">OnMetricsUpdate</a>
</td>
<td align="left" width="63%">
Called to notify the RemoteFX graphics services that network conditions have changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">IWRdsGraphicsChannel::Open</a>
 

 

