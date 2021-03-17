---
UID: NF:tsvirtualchannels.IWTSVirtualChannel.Write
title: IWTSVirtualChannel::Write (tsvirtualchannels.h)
description: Starts a write request on the channel.
helpviewer_keywords: ["IWTSVirtualChannel interface [Remote Desktop Services]","Write method","IWTSVirtualChannel.Write","IWTSVirtualChannel::Write","Write","Write method [Remote Desktop Services]","Write method [Remote Desktop Services]","IWTSVirtualChannel interface","termserv.iwtsvirtualchannel_write","tsvirtualchannels/IWTSVirtualChannel::Write"]
old-location: termserv\iwtsvirtualchannel_write.htm
tech.root: TermServ
ms.assetid: fef7067c-6d81-42b7-8534-191bc98906d4
ms.date: 12/05/2018
ms.keywords: IWTSVirtualChannel interface [Remote Desktop Services],Write method, IWTSVirtualChannel.Write, IWTSVirtualChannel::Write, Write, Write method [Remote Desktop Services], Write method [Remote Desktop Services],IWTSVirtualChannel interface, termserv.iwtsvirtualchannel_write, tsvirtualchannels/IWTSVirtualChannel::Write
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
 - IWTSVirtualChannel::Write
 - tsvirtualchannels/IWTSVirtualChannel::Write
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
 - IWTSVirtualChannel.Write
---

# IWTSVirtualChannel::Write


## -description

Starts a write request on the channel. All writes are considered asynchronous. Calling this method copies the contents of <i>pBuffer</i> and returns immediately, so  the buffer can be reclaimed. Because of the memory copy, too many <b>Write()</b> calls may result in allocating too much memory by the client.

A <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-close">Close()</a> call on this channel will cancel any pending writes.

## -parameters

### -param cbSize [in]

The size, in bytes, of the buffer to which to write.

### -param pBuffer [in]

A pointer to a buffer on the channel to which to write the data. You can reuse this buffer as soon as the call returns.

### -param pReserved [in, optional]

Reserved for future use. The value must be <b>NULL</b>.

## -returns

Returns <b>S_OK</b> if successful.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nn-tsvirtualchannels-iwtsvirtualchannel">IWTSVirtualChannel</a>