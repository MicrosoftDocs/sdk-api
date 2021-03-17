---
UID: NC:cchannel.VIRTUALCHANNELWRITE
title: VIRTUALCHANNELWRITE (cchannel.h)
description: Sends data from the client end of a virtual channel to a partner application on the server end.helpviewer_keywords: ["VirtualChannelWrite","VirtualChannelWrite callback","VirtualChannelWrite callback function [Remote Desktop Services]","_win32_virtualchannelwrite","cchannel/VirtualChannelWrite","termserv.virtualchannelwrite"]
old-location: termserv\virtualchannelwrite.htm
tech.root: TermServ
ms.assetid: bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab
ms.date: 12/05/2018
ms.keywords: VirtualChannelWrite, VirtualChannelWrite callback, VirtualChannelWrite callback function [Remote Desktop Services], _win32_virtualchannelwrite, cchannel/VirtualChannelWrite, termserv.virtualchannelwrite
req.header: cchannel.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VIRTUALCHANNELWRITE
 - cchannel/VIRTUALCHANNELWRITE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cchannel.h
api_name:
 - VirtualChannelWrite
---

# VIRTUALCHANNELWRITE callback function


## -description

Sends data from the client end of a virtual channel to a partner application on the server end.

Remote Desktop Services provides a pointer to a 
<b>VirtualChannelWrite</b> function in the 
<a href="/windows/desktop/api/cchannel/ns-cchannel-channel_entry_points">CHANNEL_ENTRY_POINTS</a> structure passed to your 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a> entry point.

## -parameters

### -param openHandle [in]

Handle to the virtual channel. This is the handle returned in the <i>pOpenHandle</i> parameter of the 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a> function.

### -param pData [in]

Pointer to a buffer containing the data to write.

### -param dataLength [in]

Specifies the number of bytes of the data in the <i>pData</i> buffer to write.

### -param pUserData [in]

An application-defined value. This value is passed to your 
<a href="/windows/desktop/api/cchannel/nc-cchannel-channel_open_event_fn">VirtualChannelOpenEvent</a> function when the write operation is completed or canceled.

## -returns

If the function succeeds, the return value is CHANNEL_RC_OK.

If an error occurs, the function returns one of the following values.

## -remarks

The 
<b>VirtualChannelWrite</b> function is asynchronous. When the write operation has been completed, your 
<a href="/windows/desktop/api/cchannel/nc-cchannel-channel_open_event_fn">VirtualChannelOpenEvent</a> function receives a CHANNEL_EVENT_WRITE_COMPLETE notification. Until that notification is received, the caller must not free or reuse the <i>pData</i> buffer passed to 
<b>VirtualChannelWrite</b>.

The value specified for the <i>pUserData</i> parameter is passed to your 
<b>VirtualChannelOpenEvent</b> function when the write operation is completed or canceled. You can use this data to identify the write operation.

The server add-in at the server end of the virtual channel calls the 
<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelread">WTSVirtualChannelRead</a> function to read the data written by a 
<b>VirtualChannelWrite</b> call.

## -see-also

<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-channel_open_event_fn">VirtualChannelOpenEvent</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsvirtualchannelread">WTSVirtualChannelRead</a>