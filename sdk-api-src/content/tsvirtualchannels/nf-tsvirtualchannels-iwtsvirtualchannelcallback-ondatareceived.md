---
UID: NF:tsvirtualchannels.IWTSVirtualChannelCallback.OnDataReceived
title: IWTSVirtualChannelCallback::OnDataReceived (tsvirtualchannels.h)
description: Notifies the user about data that is being received.
helpviewer_keywords: ["IWTSVirtualChannelCallback interface [Remote Desktop Services]","OnDataReceived method","IWTSVirtualChannelCallback.OnDataReceived","IWTSVirtualChannelCallback::OnDataReceived","OnDataReceived","OnDataReceived method [Remote Desktop Services]","OnDataReceived method [Remote Desktop Services]","IWTSVirtualChannelCallback interface","termserv.iwtsvirtualchannelcallback_ondatareceived","tsvirtualchannels/IWTSVirtualChannelCallback::OnDataReceived"]
old-location: termserv\iwtsvirtualchannelcallback_ondatareceived.htm
tech.root: TermServ
ms.assetid: 5876ba1a-3f37-4140-b448-91978aa7b0c9
ms.date: 12/05/2018
ms.keywords: IWTSVirtualChannelCallback interface [Remote Desktop Services],OnDataReceived method, IWTSVirtualChannelCallback.OnDataReceived, IWTSVirtualChannelCallback::OnDataReceived, OnDataReceived, OnDataReceived method [Remote Desktop Services], OnDataReceived method [Remote Desktop Services],IWTSVirtualChannelCallback interface, termserv.iwtsvirtualchannelcallback_ondatareceived, tsvirtualchannels/IWTSVirtualChannelCallback::OnDataReceived
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
 - IWTSVirtualChannelCallback::OnDataReceived
 - tsvirtualchannels/IWTSVirtualChannelCallback::OnDataReceived
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
 - IWTSVirtualChannelCallback.OnDataReceived
---

# IWTSVirtualChannelCallback::OnDataReceived


## -description

Notifies the user about data that is being received.

The data has the same size and content as a corresponding <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite">WTSVirtualChannelWrite()</a> call from the remote side. There is no hard limit on the size of the data that can be sent. All packet reconstruction is handled by the dynamic virtual channel (DVC) framework.

## -parameters

### -param cbSize [in]

The size, in bytes, of the buffer to receive the data.

### -param pBuffer [in]

A pointer to a buffer to receive the data. This buffer is valid only until this call is complete.

## -returns

Returns <b>S_OK</b> on success. Results in no action if the call fails.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback">IWTSVirtualChannelCallback</a>