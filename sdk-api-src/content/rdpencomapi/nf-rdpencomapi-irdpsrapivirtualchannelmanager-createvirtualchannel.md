---
UID: NF:rdpencomapi.IRDPSRAPIVirtualChannelManager.CreateVirtualChannel
title: IRDPSRAPIVirtualChannelManager::CreateVirtualChannel (rdpencomapi.h)
description: Creates a virtual channel.
helpviewer_keywords: ["CHANNEL_PRIORITY_HI","CHANNEL_PRIORITY_LO","CHANNEL_PRIORITY_MED","CreateVirtualChannel","CreateVirtualChannel method [RDP]","CreateVirtualChannel method [RDP]","IRDPSRAPIVirtualChannelManager interface","IRDPSRAPIVirtualChannelManager interface [RDP]","CreateVirtualChannel method","IRDPSRAPIVirtualChannelManager.CreateVirtualChannel","IRDPSRAPIVirtualChannelManager::CreateVirtualChannel","rdp.irdpsrapivirtualchannelmanager_createvirtualchannel","rdpencomapi/IRDPSRAPIVirtualChannelManager::CreateVirtualChannel"]
old-location: rdp\irdpsrapivirtualchannelmanager_createvirtualchannel.htm
tech.root: rdp
ms.assetid: 0185af26-a29d-4227-bad6-2633de18617e
ms.date: 12/05/2018
ms.keywords: CHANNEL_PRIORITY_HI, CHANNEL_PRIORITY_LO, CHANNEL_PRIORITY_MED, CreateVirtualChannel, CreateVirtualChannel method [RDP], CreateVirtualChannel method [RDP],IRDPSRAPIVirtualChannelManager interface, IRDPSRAPIVirtualChannelManager interface [RDP],CreateVirtualChannel method, IRDPSRAPIVirtualChannelManager.CreateVirtualChannel, IRDPSRAPIVirtualChannelManager::CreateVirtualChannel, rdp.irdpsrapivirtualchannelmanager_createvirtualchannel, rdpencomapi/IRDPSRAPIVirtualChannelManager::CreateVirtualChannel
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
 - IRDPSRAPIVirtualChannelManager::CreateVirtualChannel
 - rdpencomapi/IRDPSRAPIVirtualChannelManager::CreateVirtualChannel
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
 - IRDPSRAPIVirtualChannelManager.CreateVirtualChannel
---

# IRDPSRAPIVirtualChannelManager::CreateVirtualChannel


## -description

Creates a virtual channel.

## -parameters

### -param bstrChannelName [in]

Type: <b>BSTR</b>

The name of the channel. The maximum length is 8 characters, including the null-terminating character. Legacy channel names are limited to 32 characters.

### -param Priority [in]

Type: <b>CHANNEL_PRIORITY</b>

The priority of the channel. This parameter can be one of the following values.

<a id="CHANNEL_PRIORITY_LO"></a>
<a id="channel_priority_lo"></a>


#### CHANNEL_PRIORITY_LO

<a id="CHANNEL_PRIORITY_MED"></a>
<a id="channel_priority_med"></a>


#### CHANNEL_PRIORITY_MED

<a id="CHANNEL_PRIORITY_HI"></a>
<a id="channel_priority_hi"></a>


#### CHANNEL_PRIORITY_HI

### -param ChannelFlags [in]

Type: <b>unsigned long</b>

Flags that determine how data is sent on the channel. This parameter can be 0 or <a href="/windows/win32/api/rdpencomapi/ne-rdpencomapi-channel_flags">CHANNEL_FLAGS_UNCOMPRESSED</a>.

### -param ppChannel [out]

Type: <b>IRDPSRAPIVirtualChannel**</b>

An <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapivirtualchannel">IRDPSRAPIVirtualChannel</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code. The following is a possible value.

## -remarks

When a virtual channel is created, an RDP virtual channel is bound at the RDP stack layer for each opened channel. For a channel to actually be opened between the client and the server, both the client and the server have to bind the channel. The <i>Priority</i> parameter is used to assign a priority to the packets send on the channel.

The binding between server and client channels is established based on the channel name.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapivirtualchannelmanager">IRDPSRAPIVirtualChannelManager</a>