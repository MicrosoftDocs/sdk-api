---
UID: NN:tsvirtualchannels.IWTSVirtualChannel
title: IWTSVirtualChannel (tsvirtualchannels.h)
description: Used to control the channel state, and writes on the channel.helpviewer_keywords: ["IWTSVirtualChannel","IWTSVirtualChannel interface [Remote Desktop Services]","IWTSVirtualChannel interface [Remote Desktop Services]","described","termserv.iwtsvirtualchannel","tsvirtualchannels/IWTSVirtualChannel"]
old-location: termserv\iwtsvirtualchannel.htm
tech.root: TermServ
ms.assetid: 8a5b093f-5756-400f-9442-b95d6010ee46
ms.date: 12/05/2018
ms.keywords: IWTSVirtualChannel, IWTSVirtualChannel interface [Remote Desktop Services], IWTSVirtualChannel interface [Remote Desktop Services],described, termserv.iwtsvirtualchannel, tsvirtualchannels/IWTSVirtualChannel
f1_keywords:
- tsvirtualchannels/IWTSVirtualChannel
dev_langs:
- c++
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
- IWTSVirtualChannel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSVirtualChannel interface


## -description


Used to control the channel state, and writes on the channel. This interface is implemented by the framework.

Methods of this interface can be called from any thread.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSVirtualChannel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSVirtualChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSVirtualChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-close">Close</a>
</td>
<td align="left" width="63%">
Closes the channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-write">Write</a>
</td>
<td align="left" width="63%">
Starts a write request on the channel.

</td>
</tr>
</table> 

