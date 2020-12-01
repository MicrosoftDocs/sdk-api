---
UID: NN:wrdsgraphicschannels.IWRdsGraphicsChannel
title: IWRdsGraphicsChannel (wrdsgraphicschannels.h)
description: This interface is used by the RemoteFX graphics services to send and receive data to a virtual graphics channel.
helpviewer_keywords: ["IWRdsGraphicsChannel","IWRdsGraphicsChannel interface [Remote Desktop Services]","IWRdsGraphicsChannel interface [Remote Desktop Services]","described","termserv.iwrdsgraphicschannel","wrdsgraphicschannels/IWRdsGraphicsChannel"]
old-location: termserv\iwrdsgraphicschannel.htm
tech.root: TermServ
ms.assetid: 5d1e88b4-3dff-4f88-a6de-abc02da57ece
ms.date: 12/05/2018
ms.keywords: IWRdsGraphicsChannel, IWRdsGraphicsChannel interface [Remote Desktop Services], IWRdsGraphicsChannel interface [Remote Desktop Services],described, termserv.iwrdsgraphicschannel, wrdsgraphicschannels/IWRdsGraphicsChannel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsGraphicsChannel
 - wrdsgraphicschannels/IWRdsGraphicsChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wrdsgraphicschannels.h
api_name:
 - IWRdsGraphicsChannel
---

# IWRdsGraphicsChannel interface


## -description

This interface is used by the RemoteFX graphics services to send and receive data to a virtual graphics channel. An instance of this interface is provided to the RemoteFX graphics services in response to the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelmanager-createchannel">IWRdsGraphicsChannelManager::CreateChannel</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsGraphicsChannel</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsGraphicsChannel</b> also has these types of members:
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
<a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-close">Close</a>
</td>
<td align="left" width="63%">
Called to close the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-open">Open</a>
</td>
<td align="left" width="63%">
Called to open a channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannel-write">Write</a>
</td>
<td align="left" width="63%">
Called to send data to the virtual channel.

</td>
</tr>
</table>