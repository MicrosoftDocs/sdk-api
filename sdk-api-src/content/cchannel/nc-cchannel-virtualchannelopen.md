---
UID: NC:cchannel.VIRTUALCHANNELOPEN
title: VIRTUALCHANNELOPEN (cchannel.h)
description: Opens the client end of a virtual channel.helpviewer_keywords: ["VirtualChannelOpen","VirtualChannelOpen callback","VirtualChannelOpen callback function [Remote Desktop Services]","_win32_virtualchannelopen","cchannel/VirtualChannelOpen","termserv.virtualchannelopen"]
old-location: termserv\virtualchannelopen.htm
tech.root: TermServ
ms.assetid: 4ec75f9d-dbdf-499d-80a9-25fc6e9c5cb9
ms.date: 12/05/2018
ms.keywords: VirtualChannelOpen, VirtualChannelOpen callback, VirtualChannelOpen callback function [Remote Desktop Services], _win32_virtualchannelopen, cchannel/VirtualChannelOpen, termserv.virtualchannelopen
f1_keywords:
- cchannel/VirtualChannelOpen
dev_langs:
- c++
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
- UserDefined
api_location:
- Cchannel.h
api_name:
- VirtualChannelOpen
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VIRTUALCHANNELOPEN callback function


## -description


Opens the client end of a virtual channel.

Remote Desktop Services provides a pointer to a 
<b>VirtualChannelOpen</b> function in the 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/ns-cchannel-channel_entry_points">CHANNEL_ENTRY_POINTS</a> structure passed to your 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a> entry point.


## -parameters




### -param pInitHandle [in]

Handle to the client connection. This is the handle returned in the <i>ppInitHandle</i> parameter of the 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a> function.


### -param pOpenHandle [out]

Pointer to a variable that receives a handle that identifies the open virtual channel in subsequent calls to the 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelclose">VirtualChannelClose</a> functions.


### -param pChannelName [in]

Pointer to a null-terminated ANSI character string containing the name of the virtual channel to open. The name must have been registered when the client called the 
<b>VirtualChannelInit</b> function.


### -param pChannelOpenEventProc [in]

Pointer to an application-defined 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-channel_open_event_fn">VirtualChannelOpenEvent</a> function that Remote Desktop Services calls to notify the client DLL of events for this virtual channel.


## -returns



If the function succeeds, the return value is CHANNEL_RC_OK.

If an error occurs, the function returns one of the following values.




## -remarks



The client DLL cannot call this function until the client has established a connection with an RD Session Host 
    server. Your <a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-channel_init_event_fn">VirtualChannelInitEvent</a> 
    function receives a CHANNEL_EVENT_CONNECTED notification when an RD Session Host server connection is established.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelclose">VirtualChannelClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-channel_init_event_fn">VirtualChannelInitEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-channel_open_event_fn">VirtualChannelOpenEvent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelwrite">VirtualChannelWrite</a>
 

 

