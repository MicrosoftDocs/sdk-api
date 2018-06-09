---
UID: NS:cchannel.tagCHANNEL_ENTRY_POINTS
title: tagCHANNEL_ENTRY_POINTS
author: windows-sdk-content
description: Contains pointers to the functions called by a client-side DLL to access virtual channels.
old-location: termserv\channel_entry_points_str.htm
old-project: TermServ
ms.assetid: f64471b0-1f2e-48cb-9f9c-1bb536afc248
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PCHANNEL_ENTRY_POINTS, CHANNEL_ENTRY_POINTS, CHANNEL_ENTRY_POINTS structure [Remote Desktop Services], PCHANNEL_ENTRY_POINTS, PCHANNEL_ENTRY_POINTS structure pointer [Remote Desktop Services], _win32_channel_entry_points_str, cchannel/CHANNEL_ENTRY_POINTS, cchannel/PCHANNEL_ENTRY_POINTS, tagCHANNEL_ENTRY_POINTS, termserv.channel_entry_points_str"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CHANNEL_ENTRY_POINTS, *PCHANNEL_ENTRY_POINTS
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
req.lib: 
req.dll: 
req.irql: 
---

# tagCHANNEL_ENTRY_POINTS structure


## -description


Contains pointers to the functions called by a client-side DLL to access virtual channels.Remote Desktop Services calls your 
<a href="https://msdn.microsoft.com/1fd185fb-6dc9-4b32-9fa7-15ef76776305">VirtualChannelEntry</a> function to pass this structure.


## -struct-fields




### -field cbSize

Size, in bytes, of this structure.


### -field protocolVersion

Protocol version. Remote Desktop Services sets this member to <b>VIRTUAL_CHANNEL_VERSION_WIN2000</b>.


### -field pVirtualChannelInit

Pointer to a 
<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a> function.


### -field pVirtualChannelOpen

Pointer to a 
<a href="https://msdn.microsoft.com/4ec75f9d-dbdf-499d-80a9-25fc6e9c5cb9">VirtualChannelOpen</a> function.


### -field pVirtualChannelClose

Pointer to a 
<a href="https://msdn.microsoft.com/96fd8910-6cc7-460c-9f63-3363fbbae0b1">VirtualChannelClose</a> function.


### -field pVirtualChannelWrite

Pointer to a 
<a href="https://msdn.microsoft.com/bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab">VirtualChannelWrite</a> function.


## -see-also




<a href="https://msdn.microsoft.com/96fd8910-6cc7-460c-9f63-3363fbbae0b1">VirtualChannelClose</a>



<a href="https://msdn.microsoft.com/1fd185fb-6dc9-4b32-9fa7-15ef76776305">VirtualChannelEntry</a>



<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a>



<a href="https://msdn.microsoft.com/4ec75f9d-dbdf-499d-80a9-25fc6e9c5cb9">VirtualChannelOpen</a>



<a href="https://msdn.microsoft.com/bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab">VirtualChannelWrite</a>
 

 

