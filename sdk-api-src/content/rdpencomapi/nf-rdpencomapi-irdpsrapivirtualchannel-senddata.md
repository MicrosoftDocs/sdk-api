---
UID: NF:rdpencomapi.IRDPSRAPIVirtualChannel.SendData
title: IRDPSRAPIVirtualChannel::SendData (rdpencomapi.h)
description: Sends data on the channel.
helpviewer_keywords: ["CHANNEL_FLAGS_UNCOMPRESSED","IRDPSRAPIVirtualChannel interface [RDP]","SendData method","IRDPSRAPIVirtualChannel.SendData","IRDPSRAPIVirtualChannel::SendData","SendData","SendData method [RDP]","SendData method [RDP]","IRDPSRAPIVirtualChannel interface","rdp.irdpsrapivirtualchannel_senddata","rdpencomapi/IRDPSRAPIVirtualChannel::SendData"]
old-location: rdp\irdpsrapivirtualchannel_senddata.htm
tech.root: rdp
ms.assetid: d861de01-70e3-49b0-91b3-01f6b0051823
ms.date: 12/05/2018
ms.keywords: CHANNEL_FLAGS_UNCOMPRESSED, IRDPSRAPIVirtualChannel interface [RDP],SendData method, IRDPSRAPIVirtualChannel.SendData, IRDPSRAPIVirtualChannel::SendData, SendData, SendData method [RDP], SendData method [RDP],IRDPSRAPIVirtualChannel interface, rdp.irdpsrapivirtualchannel_senddata, rdpencomapi/IRDPSRAPIVirtualChannel::SendData
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIVirtualChannel::SendData
 - rdpencomapi/IRDPSRAPIVirtualChannel::SendData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIVirtualChannel.SendData
---

# IRDPSRAPIVirtualChannel::SendData


## -description

Sends data on the channel.

## -parameters

### -param bstrData [in]

Type: <b>BSTR</b>

The buffer to be sent in a packet on the channel. The maximum size  of the data is CONST_MAX_MESSAGE_SIZE bytes.

### -param lAttendeeId [in]

Type: <b>long</b>

The attendee that should receive the data. To send the data to all attendees, use CONST_ATTENDEE_ID_EVERYONE.

### -param ChannelSendFlags [in]

Type: <b>unsigned long</b>

The channel flags. This parameter can be 0 or the following value.



#### CHANNEL_FLAGS_UNCOMPRESSED

The data should not be compressed before it is sent because it is in a format that is already compressed.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapivirtualchannel">IRDPSRAPIVirtualChannel</a>