---
UID: NS:cchannel.tagCHANNEL_ENTRY_POINTS
title: tagCHANNEL_ENTRY_POINTS
author: windows-sdk-content
description: Contains pointers to the functions called by a client-side DLL to access virtual channels.
old-location: termserv\channel_entry_points_str.htm
tech.root: termserv
ms.assetid: f64471b0-1f2e-48cb-9f9c-1bb536afc248
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PCHANNEL_ENTRY_POINTS, CHANNEL_ENTRY_POINTS, CHANNEL_ENTRY_POINTS structure [Remote Desktop Services], PCHANNEL_ENTRY_POINTS, PCHANNEL_ENTRY_POINTS structure pointer [Remote Desktop Services], _win32_channel_entry_points_str, cchannel/CHANNEL_ENTRY_POINTS, cchannel/PCHANNEL_ENTRY_POINTS, tagCHANNEL_ENTRY_POINTS, termserv.channel_entry_points_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cchannel.h
api_name:
 - CHANNEL_ENTRY_POINTS
product: Windows
targetos: Windows
req.typenames: CHANNEL_ENTRY_POINTS, *PCHANNEL_ENTRY_POINTS
req.redist: 
---

# tagCHANNEL_ENTRY_POINTS structure


## -description


Contains pointers to the functions called by a client-side DLL to access virtual channels.Remote Desktop Services calls your 
<a href="https://msdn.microsoft.com/en-us/library/Aa383560(v=VS.85).aspx">VirtualChannelEntry</a> function to pass this structure.


## -struct-fields




### -field cbSize

Size, in bytes, of this structure.


### -field protocolVersion

Protocol version. Remote Desktop Services sets this member to <b>VIRTUAL_CHANNEL_VERSION_WIN2000</b>.


### -field pVirtualChannelInit

Pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/Aa383564(v=VS.85).aspx">VirtualChannelInit</a> function.


### -field pVirtualChannelOpen

Pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/Aa383570(v=VS.85).aspx">VirtualChannelOpen</a> function.


### -field pVirtualChannelClose

Pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/Aa383556(v=VS.85).aspx">VirtualChannelClose</a> function.


### -field pVirtualChannelWrite

Pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/Aa383576(v=VS.85).aspx">VirtualChannelWrite</a> function.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383556(v=VS.85).aspx">VirtualChannelClose</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383560(v=VS.85).aspx">VirtualChannelEntry</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383564(v=VS.85).aspx">VirtualChannelInit</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383570(v=VS.85).aspx">VirtualChannelOpen</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383576(v=VS.85).aspx">VirtualChannelWrite</a>
 

 

