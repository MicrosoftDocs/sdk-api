---
UID: NS:pchannel.tagCHANNEL_PDU_HEADER
title: CHANNEL_PDU_HEADER (pchannel.h)
description: Contains information about a data block being received by the server end of a virtual channel.
helpviewer_keywords: ["*PCHANNEL_PDU_HEADER","CHANNEL_FLAG_FIRST","CHANNEL_FLAG_LAST","CHANNEL_FLAG_MIDDLE","CHANNEL_FLAG_ONLY","CHANNEL_PDU_HEADER","CHANNEL_PDU_HEADER structure [Remote Desktop Services]","PCHANNEL_PDU_HEADER","PCHANNEL_PDU_HEADER structure pointer [Remote Desktop Services]","_win32_channel_pdu_header_str","pchannel/CHANNEL_PDU_HEADER","pchannel/PCHANNEL_PDU_HEADER","termserv.channel_pdu_header_str"]
old-location: termserv\channel_pdu_header_str.htm
tech.root: TermServ
ms.assetid: f980e746-fc05-45e8-af27-6f137ef01bf9
ms.date: 12/05/2018
ms.keywords: '*PCHANNEL_PDU_HEADER, CHANNEL_FLAG_FIRST, CHANNEL_FLAG_LAST, CHANNEL_FLAG_MIDDLE, CHANNEL_FLAG_ONLY, CHANNEL_PDU_HEADER, CHANNEL_PDU_HEADER structure [Remote Desktop Services], PCHANNEL_PDU_HEADER, PCHANNEL_PDU_HEADER structure pointer [Remote Desktop Services], _win32_channel_pdu_header_str, pchannel/CHANNEL_PDU_HEADER, pchannel/PCHANNEL_PDU_HEADER, termserv.channel_pdu_header_str'
req.header: pchannel.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CHANNEL_PDU_HEADER, *PCHANNEL_PDU_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCHANNEL_PDU_HEADER
 - pchannel/tagCHANNEL_PDU_HEADER
 - PCHANNEL_PDU_HEADER
 - pchannel/PCHANNEL_PDU_HEADER
 - CHANNEL_PDU_HEADER
 - pchannel/CHANNEL_PDU_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pchannel.h
api_name:
 - CHANNEL_PDU_HEADER
---

# CHANNEL_PDU_HEADER structure


## -description

Contains information about a data block being received by the server end of a virtual channel.

## -struct-fields

### -field length

Size, in bytes, of the data block, excluding this header.

### -field flags

Information about the data block. The following bit flags will be set. Note that you should not make direct 
      comparisons using the '==' operator when comparing the values in the following list; instead, use the comparison 
      methods described in the list.



#### CHANNEL_FLAG_FIRST (1)

The chunk is the beginning of the data written by a single write operation.

Use bitwise comparisons when comparing this flag.



#### CHANNEL_FLAG_LAST (2)

The chunk is the end of the data written by a single write operation.

Use bitwise comparisons when comparing this flag.



#### CHANNEL_FLAG_MIDDLE (0)

This is the default. The chunk is in the middle of a block of data written by a single write operation.

Do not use bitwise comparisons to compare this flag value directly. Instead, use bitwise comparisons to 
         determine that the flag value is not <b>CHANNEL_FLAG_FIRST</b> or 
         <b>CHANNEL_FLAG_LAST</b>. This is done by using the following comparison:

<code>Result = !(flags &amp; CHANNEL_FLAG_FIRST) &amp;&amp; !(flags &amp; CHANNEL_FLAG_LAST)</code>



#### CHANNEL_FLAG_ONLY (3)

Combines the <b>CHANNEL_FLAG_FIRST</b> and <b>CHANNEL_FLAG_LAST</b> values. The chunk contains all the data from a single write operation.

Use bitwise comparisons when comparing this flag.

## -remarks

In certain cases, Remote Desktop Services places a 
    <b>CHANNEL_PDU_HEADER</b> structure at the beginning 
    of each chunk of data read by a call to the 
    <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelread">WTSVirtualChannelRead</a> function. This will 
    occur if the client DLL sets the <b>CHANNEL_OPTION_SHOW_PROTOCOL</b> option when it calls the 
    <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a> function to initialize the 
    virtual channel. This will also occur if the channel is a dynamic virtual channel written to by using the 
    <a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-write">IWTSVirtualChannel::Write</a> method.

## -see-also

<a href="/windows/desktop/api/tsvirtualchannels/nf-tsvirtualchannels-iwtsvirtualchannel-write">IWTSVirtualChannel::Write</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelread">WTSVirtualChannelRead</a>