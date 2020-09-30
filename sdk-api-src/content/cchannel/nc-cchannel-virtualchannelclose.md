---
UID: NC:cchannel.VIRTUALCHANNELCLOSE
title: VIRTUALCHANNELCLOSE (cchannel.h)
description: Closes the client end of a virtual channel.
helpviewer_keywords: ["VirtualChannelClose","VirtualChannelClose callback","VirtualChannelClose callback function [Remote Desktop Services]","_win32_virtualchannelclose","cchannel/VirtualChannelClose","termserv.virtualchannelclose"]
old-location: termserv\virtualchannelclose.htm
tech.root: TermServ
ms.assetid: 96fd8910-6cc7-460c-9f63-3363fbbae0b1
ms.date: 12/05/2018
ms.keywords: VirtualChannelClose, VirtualChannelClose callback, VirtualChannelClose callback function [Remote Desktop Services], _win32_virtualchannelclose, cchannel/VirtualChannelClose, termserv.virtualchannelclose
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
 - VIRTUALCHANNELCLOSE
 - cchannel/VIRTUALCHANNELCLOSE
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
 - VirtualChannelClose
---

# VIRTUALCHANNELCLOSE callback function


## -description

Closes the client end of a virtual channel.

Remote Desktop Services provides a pointer to a 
<b>VirtualChannelClose</b> function in the 
<a href="/windows/desktop/api/cchannel/ns-cchannel-channel_entry_points">CHANNEL_ENTRY_POINTS</a> structure passed to your 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a> entry point.

## -parameters

### -param openHandle [in]

Handle to the virtual channel. This is the handle returned in the <i>pOpenHandle</i> parameter of the 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a> function.

## -returns

If the function succeeds, the return value is CHANNEL_RC_OK.

If an error occurs, the function returns one of the following values.

## -see-also

<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a>