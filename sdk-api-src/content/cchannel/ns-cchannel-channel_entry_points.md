---
UID: NS:cchannel.tagCHANNEL_ENTRY_POINTS
title: CHANNEL_ENTRY_POINTS (cchannel.h)
description: Contains pointers to the functions called by a client-side DLL to access virtual channels.
helpviewer_keywords: ["*PCHANNEL_ENTRY_POINTS","CHANNEL_ENTRY_POINTS","CHANNEL_ENTRY_POINTS structure [Remote Desktop Services]","PCHANNEL_ENTRY_POINTS","PCHANNEL_ENTRY_POINTS structure pointer [Remote Desktop Services]","_win32_channel_entry_points_str","cchannel/CHANNEL_ENTRY_POINTS","cchannel/PCHANNEL_ENTRY_POINTS","termserv.channel_entry_points_str"]
old-location: termserv\channel_entry_points_str.htm
tech.root: TermServ
ms.assetid: f64471b0-1f2e-48cb-9f9c-1bb536afc248
ms.date: 12/05/2018
ms.keywords: '*PCHANNEL_ENTRY_POINTS, CHANNEL_ENTRY_POINTS, CHANNEL_ENTRY_POINTS structure [Remote Desktop Services], PCHANNEL_ENTRY_POINTS, PCHANNEL_ENTRY_POINTS structure pointer [Remote Desktop Services], _win32_channel_entry_points_str, cchannel/CHANNEL_ENTRY_POINTS, cchannel/PCHANNEL_ENTRY_POINTS, termserv.channel_entry_points_str'
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
req.typenames: CHANNEL_ENTRY_POINTS, *PCHANNEL_ENTRY_POINTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCHANNEL_ENTRY_POINTS
 - cchannel/tagCHANNEL_ENTRY_POINTS
 - PCHANNEL_ENTRY_POINTS
 - cchannel/PCHANNEL_ENTRY_POINTS
 - CHANNEL_ENTRY_POINTS
 - cchannel/CHANNEL_ENTRY_POINTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cchannel.h
api_name:
 - CHANNEL_ENTRY_POINTS
---

# CHANNEL_ENTRY_POINTS structure


## -description

Contains pointers to the functions called by a client-side DLL to access virtual channels.Remote Desktop Services calls your 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a> function to pass this structure.

## -struct-fields

### -field cbSize

Size, in bytes, of this structure.

### -field protocolVersion

Protocol version. Remote Desktop Services sets this member to <b>VIRTUAL_CHANNEL_VERSION_WIN2000</b>.

### -field pVirtualChannelInit

Pointer to a 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a> function.

### -field pVirtualChannelOpen

Pointer to a 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a> function.

### -field pVirtualChannelClose

Pointer to a 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelclose">VirtualChannelClose</a> function.

### -field pVirtualChannelWrite

Pointer to a 
<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a> function.

## -see-also

<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelclose">VirtualChannelClose</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a>