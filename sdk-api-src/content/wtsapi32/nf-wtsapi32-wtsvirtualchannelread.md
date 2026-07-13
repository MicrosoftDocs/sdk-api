---
UID: NF:wtsapi32.WTSVirtualChannelRead
title: WTSVirtualChannelRead function (wtsapi32.h)
description: Reads data from the server end of a virtual channel.
helpviewer_keywords: ["WTSVirtualChannelRead","WTSVirtualChannelRead function [Remote Desktop Services]","_win32_wtsvirtualchannelread","termserv.wtsvirtualchannelread","wtsapi32/WTSVirtualChannelRead"]
old-location: termserv\wtsvirtualchannelread.htm
tech.root: TermServ
ms.assetid: 7434e761-303f-496f-81cb-83c199ddec8a
ms.date: 12/05/2018
ms.keywords: WTSVirtualChannelRead, WTSVirtualChannelRead function [Remote Desktop Services], _win32_wtsvirtualchannelread, termserv.wtsvirtualchannelread, wtsapi32/WTSVirtualChannelRead
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.Dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTSVirtualChannelRead
 - wtsapi32/WTSVirtualChannelRead
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-session-wtsapi32-l1-1-1.dll
 - Wtsapi32.Dll
api_name:
 - WTSVirtualChannelRead
---

# WTSVirtualChannelRead function


## -description

Reads data from the server end of a virtual
   channel.

<b>WTSVirtualChannelRead</b> reads the data written 
    by a <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a> call at the client 
    end of the virtual channel.

## -parameters

### -param hChannelHandle [in]

Handle to a virtual channel opened by the 
      <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelopen">WTSVirtualChannelOpen</a> function.

### -param TimeOut [in]

Specifies the time-out, in milliseconds. If <i>TimeOut</i> is zero, 
      <b>WTSVirtualChannelRead</b> returns immediately 
      if there is no data to read. If <i>TimeOut</i> is INFINITE (defined in Winbase.h), the 
      function waits indefinitely until there is data to read.

### -param Buffer [out]

Pointer to a buffer that receives a chunk of data read from the server end of the virtual channel. The maximum 
      amount of data that the server can receive in a single 
      <b>WTSVirtualChannelRead</b> call is 
      <b>CHANNEL_CHUNK_LENGTH</b> bytes. If the client's 
      <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a> call writes 
      a larger block of data, the server must make multiple 
      <b>WTSVirtualChannelRead</b> calls.

In certain cases, Remote Desktop Services places a 
<b>CHANNEL_PDU_HEADER</b> structure at the beginning of each chunk of data read by the 
<b>WTSVirtualChannelRead</b> function. This will occur if the 
client DLL sets the <b>CHANNEL_OPTION_SHOW_PROTOCOL</b> option when it calls the 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a> function to initialize the virtual channel. This will also occur if the channel is a dynamic virtual channel written to by using the <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-write">IWTSVirtualChannel::Write</a> method. Otherwise, 
       the buffer receives only the data written in the 
       <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a> call.

### -param BufferSize [in]

Specifies the size, in bytes, of <i>Buffer</i>. If the chunk of data in <i>Buffer</i> will be preceded by a <b>CHANNEL_PDU_HEADER</b> structure, the value of this parameter should be at least 
      <b>CHANNEL_PDU_LENGTH</b>. Otherwise, the value of this parameter should be at least <b>CHANNEL_CHUNK_LENGTH</b>.

### -param pBytesRead [out]

Pointer to a variable that receives the number of bytes read.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  <b>WTSVirtualChannelRead</b> is not thread safe. 
    To access a virtual channel from multiple threads, or to do asynchronous IO through a virtual channel, use 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelquery">WTSVirtualChannelQuery</a> with 
    <b>WTSVirtualFileHandle</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/pchannel/ns-pchannel-channel_pdu_header">CHANNEL_PDU_HEADER</a>



<a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-write">IWTSVirtualChannel::Write</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelquery">WTSVirtualChannelQuery</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite">WTSVirtualChannelWrite</a>