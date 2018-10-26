---
UID: NC:cchannel.VIRTUALCHANNELINIT
title: VIRTUALCHANNELINIT
author: windows-sdk-content
description: Initializes a client DLL's access to Remote Desktop Services virtual channels.
old-location: termserv\virtualchannelinit.htm
tech.root: termserv
ms.assetid: 3dae59dc-e70f-450e-a324-a4d68341a72e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: VirtualChannelInit, VirtualChannelInit callback, VirtualChannelInit callback function [Remote Desktop Services], _win32_virtualchannelinit, cchannel/VirtualChannelInit, termserv.virtualchannelinit
ms.prod: windows
ms.technology: windows-sdk
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
 - VirtualChannelInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VIRTUALCHANNELINIT callback function


## -description


Initializes a client DLL's access to Remote Desktop Services virtual channels. The client calls <b>VirtualChannelInit</b> to register the 
    names of its virtual channels.

Remote Desktop Services provides a pointer to a <b>VirtualChannelInit</b> function in the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa380779(v=VS.85).aspx">CHANNEL_ENTRY_POINTS</a> structure passed to 
    your <a href="https://msdn.microsoft.com/en-us/library/Aa383560(v=VS.85).aspx">VirtualChannelEntry</a> entry point.


## -parameters




### -param *ppInitHandle [in]

Pointer to a variable that receives a handle that identifies the client connection. Use this handle to 
      identify the client in subsequent calls to the 
      <a href="https://msdn.microsoft.com/en-us/library/Aa383570(v=VS.85).aspx">VirtualChannelOpen</a> function.


### -param pChannel [in, out]

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Aa380685(v=VS.85).aspx">CHANNEL_DEF</a> 
      structures. Each structure contains the name and initialization options of a virtual channel that the client 
      DLL will open. Note that the <b>VirtualChannelInit</b> call does not open these 
      virtual channels; it only reserves the names for use by this application.


### -param channelCount [in]

Specifies the number of entries in the <i>pChannel</i> array.


### -param versionRequested [in]

Specifies the level of virtual channel support. Set this parameter to <b>VIRTUAL_CHANNEL_VERSION_WIN2000</b>.


### -param pChannelInitEventProc [in]

Pointer to an application-defined 
      <a href="https://msdn.microsoft.com/en-us/library/Aa383568(v=VS.85).aspx">VirtualChannelInitEvent</a> function that 
      Remote Desktop Services calls to notify the client DLL of virtual channel events.


## -returns



If the function succeeds, the return value is <b>CHANNEL_RC_OK</b>.

If an error occurs, the function returns one of the following values.




## -remarks



You can call the <b>VirtualChannelInit</b> function only from your 
   <a href="https://msdn.microsoft.com/en-us/library/Aa383560(v=VS.85).aspx">VirtualChannelEntry</a> function. 
   Calls to <b>VirtualChannelInit</b> at any other time fail.

When <b>VirtualChannelInit</b> returns successfully, Remote Desktop Services has 
   registered the requested channels. However, Remote Desktop Services may not have completed other initialization. When 
   all initialization is complete, Remote Desktop Services calls your 
   <a href="https://msdn.microsoft.com/en-us/library/Aa383568(v=VS.85).aspx">VirtualChannelInitEvent</a> 
   callback function with the <b>CHANNEL_EVENT_INITIALIZED</b> event.

You should not make assumptions about the number of available virtual channels before calling this function, 
   because the system and other plug-ins may have reserved virtual channels. Therefore, you should always check for a 
   <b>CHANNEL_RC_TOO_MANY_CHANNELS</b> return code after calling this function.

When <b>VirtualChannelInit</b> returns, the <b>options</b> member of each 
   <a href="https://msdn.microsoft.com/en-us/library/Aa380685(v=VS.85).aspx">CHANNEL_DEF</a> structure includes 
   <b>CHANNEL_OPTION_INITIALIZED</b> if the channel was successfully initialized.

The maximum number of channels per client session is <b>CHANNEL_MAX_COUNT</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380685(v=VS.85).aspx">CHANNEL_DEF</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383560(v=VS.85).aspx">VirtualChannelEntry</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383568(v=VS.85).aspx">VirtualChannelInitEvent</a>
 

 

