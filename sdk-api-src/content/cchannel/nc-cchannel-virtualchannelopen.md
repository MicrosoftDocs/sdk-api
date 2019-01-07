---
UID: NC:cchannel.VIRTUALCHANNELOPEN
title: VIRTUALCHANNELOPEN
author: windows-sdk-content
description: Opens the client end of a virtual channel.
old-location: termserv\virtualchannelopen.htm
tech.root: termserv
ms.assetid: 4ec75f9d-dbdf-499d-80a9-25fc6e9c5cb9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VirtualChannelOpen, VirtualChannelOpen callback, VirtualChannelOpen callback function [Remote Desktop Services], _win32_virtualchannelopen, cchannel/VirtualChannelOpen, termserv.virtualchannelopen
ms.topic: callback
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VIRTUALCHANNELOPEN callback function


## -description


Opens the client end of a virtual channel.

Remote Desktop Services provides a pointer to a 
<b>VirtualChannelOpen</b> function in the 
<a href="https://msdn.microsoft.com/f64471b0-1f2e-48cb-9f9c-1bb536afc248">CHANNEL_ENTRY_POINTS</a> structure passed to your 
<a href="https://msdn.microsoft.com/1fd185fb-6dc9-4b32-9fa7-15ef76776305">VirtualChannelEntry</a> entry point.


## -parameters




### -param pInitHandle [in]

Handle to the client connection. This is the handle returned in the <i>ppInitHandle</i> parameter of the 
<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a> function.


### -param pOpenHandle [out]

Pointer to a variable that receives a handle that identifies the open virtual channel in subsequent calls to the 
<a href="https://msdn.microsoft.com/bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab">VirtualChannelWrite</a> and 
<a href="https://msdn.microsoft.com/96fd8910-6cc7-460c-9f63-3363fbbae0b1">VirtualChannelClose</a> functions.


### -param pChannelName [in]

Pointer to a null-terminated ANSI character string containing the name of the virtual channel to open. The name must have been registered when the client called the 
<b>VirtualChannelInit</b> function.


### -param pChannelOpenEventProc [in]

Pointer to an application-defined 
<a href="https://msdn.microsoft.com/7412d125-1a3c-4e9a-9804-b612030682da">VirtualChannelOpenEvent</a> function that Remote Desktop Services calls to notify the client DLL of events for this virtual channel.


## -returns



If the function succeeds, the return value is CHANNEL_RC_OK.

If an error occurs, the function returns one of the following values.




## -remarks



The client DLL cannot call this function until the client has established a connection with an RD Session Host 
    server. Your <a href="https://msdn.microsoft.com/8a074b6c-7fc1-411f-a50c-64f40c0c4dd6">VirtualChannelInitEvent</a> 
    function receives a CHANNEL_EVENT_CONNECTED notification when an RD Session Host server connection is established.




## -see-also




<a href="https://msdn.microsoft.com/96fd8910-6cc7-460c-9f63-3363fbbae0b1">VirtualChannelClose</a>



<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a>



<a href="https://msdn.microsoft.com/8a074b6c-7fc1-411f-a50c-64f40c0c4dd6">VirtualChannelInitEvent</a>



<a href="https://msdn.microsoft.com/7412d125-1a3c-4e9a-9804-b612030682da">VirtualChannelOpenEvent</a>



<a href="https://msdn.microsoft.com/bd7bc65e-403c-4e29-bdb4-f2f5a957d6ab">VirtualChannelWrite</a>
 

 

