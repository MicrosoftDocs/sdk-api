---
UID: NF:tsvirtualchannels.IWTSVirtualChannel.Close
title: IWTSVirtualChannel::Close (tsvirtualchannels.h)
description: Closes the channel. (IWTSVirtualChannel.Close)
helpviewer_keywords: ["Close","Close method [Remote Desktop Services]","Close method [Remote Desktop Services]","IWTSVirtualChannel interface","IWTSVirtualChannel interface [Remote Desktop Services]","Close method","IWTSVirtualChannel.Close","IWTSVirtualChannel::Close","termserv.iwtsvirtualchannel_close","tsvirtualchannels/IWTSVirtualChannel::Close"]
old-location: termserv\iwtsvirtualchannel_close.htm
tech.root: TermServ
ms.assetid: b900789d-c7da-4974-8c46-72ea8ffd6892
ms.date: 12/05/2018
ms.keywords: Close, Close method [Remote Desktop Services], Close method [Remote Desktop Services],IWTSVirtualChannel interface, IWTSVirtualChannel interface [Remote Desktop Services],Close method, IWTSVirtualChannel.Close, IWTSVirtualChannel::Close, termserv.iwtsvirtualchannel_close, tsvirtualchannels/IWTSVirtualChannel::Close
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSVirtualChannel::Close
 - tsvirtualchannels/IWTSVirtualChannel::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSVirtualChannel.Close
---

# IWTSVirtualChannel::Close


## -description

Closes the channel.

If the channel has not already been closed, the <b>Close()</b> method will call the <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannelcallback-onclose">IWTSVirtualChannelCallback::OnClose()</a> method into the associated virtual channel callback interface. After a channel is closed, any <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-write">Write()</a> call on it will fail.



## -returns

Returns <b>S_OK</b> if successful.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannel">IWTSVirtualChannel</a>
