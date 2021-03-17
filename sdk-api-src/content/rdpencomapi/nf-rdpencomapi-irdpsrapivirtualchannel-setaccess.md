---
UID: NF:rdpencomapi.IRDPSRAPIVirtualChannel.SetAccess
title: IRDPSRAPIVirtualChannel::SetAccess (rdpencomapi.h)
description: Enables the channel for an attendee.
helpviewer_keywords: ["CHANNEL_ACCESS_ENUM_NONE","CHANNEL_ACCESS_ENUM_SENDRECEIVE","IRDPSRAPIVirtualChannel interface [RDP]","SetAccess method","IRDPSRAPIVirtualChannel.SetAccess","IRDPSRAPIVirtualChannel::SetAccess","SetAccess","SetAccess method [RDP]","SetAccess method [RDP]","IRDPSRAPIVirtualChannel interface","rdp.irdpsrapivirtualchannel_setaccess","rdpencomapi/IRDPSRAPIVirtualChannel::SetAccess"]
old-location: rdp\irdpsrapivirtualchannel_setaccess.htm
tech.root: rdp
ms.assetid: 7d4a19d3-b089-4689-9062-a5b52251776f
ms.date: 12/05/2018
ms.keywords: CHANNEL_ACCESS_ENUM_NONE, CHANNEL_ACCESS_ENUM_SENDRECEIVE, IRDPSRAPIVirtualChannel interface [RDP],SetAccess method, IRDPSRAPIVirtualChannel.SetAccess, IRDPSRAPIVirtualChannel::SetAccess, SetAccess, SetAccess method [RDP], SetAccess method [RDP],IRDPSRAPIVirtualChannel interface, rdp.irdpsrapivirtualchannel_setaccess, rdpencomapi/IRDPSRAPIVirtualChannel::SetAccess
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
 - IRDPSRAPIVirtualChannel::SetAccess
 - rdpencomapi/IRDPSRAPIVirtualChannel::SetAccess
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
 - IRDPSRAPIVirtualChannel.SetAccess
---

# IRDPSRAPIVirtualChannel::SetAccess


## -description

Enables the channel for an attendee.

## -parameters

### -param lAttendeeId [in]

Type: <b>long</b>

The identifier of the attendee.

### -param AccessType [in]

Type: <b>CHANNEL_ACCESS_ENUM</b>

The type of access granted. This parameter can be one of the following values.

<a id="CHANNEL_ACCESS_ENUM_NONE"></a>
<a id="channel_access_enum_none"></a>


#### CHANNEL_ACCESS_ENUM_NONE

<a id="CHANNEL_ACCESS_ENUM_SENDRECEIVE"></a>
<a id="channel_access_enum_sendreceive"></a>


#### CHANNEL_ACCESS_ENUM_SENDRECEIVE

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -remarks

This method must be called for each attendee that will receive data over the channel.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapivirtualchannel">IRDPSRAPIVirtualChannel</a>