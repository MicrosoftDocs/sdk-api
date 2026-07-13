---
UID: NC:cchannel.VIRTUALCHANNELINIT
title: VIRTUALCHANNELINIT (cchannel.h)
description: Initializes a client DLL's access to Remote Desktop Services virtual channels.
helpviewer_keywords: ["VirtualChannelInit","VirtualChannelInit callback","VirtualChannelInit callback function [Remote Desktop Services]","_win32_virtualchannelinit","cchannel/VirtualChannelInit","termserv.virtualchannelinit"]
old-location: termserv\virtualchannelinit.htm
tech.root: TermServ
ms.assetid: 3dae59dc-e70f-450e-a324-a4d68341a72e
ms.date: 12/05/2018
ms.keywords: VirtualChannelInit, VirtualChannelInit callback, VirtualChannelInit callback function [Remote Desktop Services], _win32_virtualchannelinit, cchannel/VirtualChannelInit, termserv.virtualchannelinit
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
 - VIRTUALCHANNELINIT
 - cchannel/VIRTUALCHANNELINIT
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
 - VirtualChannelInit
---

# VIRTUALCHANNELINIT callback function


## -description

Initializes a client DLL's access to Remote Desktop Services virtual channels. The client calls <b>VirtualChannelInit</b> to register the 
    names of its virtual channels.

Remote Desktop Services provides a pointer to a <b>VirtualChannelInit</b> function in the 
    <a href="/windows/desktop/api/cchannel/ns-cchannel-channel_entry_points">CHANNEL_ENTRY_POINTS</a> structure passed to 
    your <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a> entry point.

## -parameters

### -param ppInitHandle [in]

Pointer to a variable that receives a handle that identifies the client connection. Use this handle to 
      identify the client in subsequent calls to the 
      <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelopen">VirtualChannelOpen</a> function.

### -param pChannel [in, out]

Pointer to an array of <a href="/previous-versions/windows/embedded/aa513856(v=msdn.10)">CHANNEL_DEF</a> 
      structures. Each structure contains the name and initialization options of a virtual channel that the client 
      DLL will open. Note that the <b>VirtualChannelInit</b> call does not open these 
      virtual channels; it only reserves the names for use by this application.

### -param channelCount [in]

Specifies the number of entries in the <i>pChannel</i> array.

### -param versionRequested [in]

Specifies the level of virtual channel support. Set this parameter to <b>VIRTUAL_CHANNEL_VERSION_WIN2000</b>.

### -param pChannelInitEventProc [in]

Pointer to an application-defined 
      <a href="/windows/desktop/api/cchannel/nc-cchannel-channel_init_event_fn">VirtualChannelInitEvent</a> function that 
      Remote Desktop Services calls to notify the client DLL of virtual channel events.

## -returns

If the function succeeds, the return value is <b>CHANNEL_RC_OK</b>.

If an error occurs, the function returns one of the following values.

## -remarks

You can call the <b>VirtualChannelInit</b> function only from your 
   <a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a> function. 
   Calls to <b>VirtualChannelInit</b> at any other time fail.

When <b>VirtualChannelInit</b> returns successfully, Remote Desktop Services has 
   registered the requested channels. However, Remote Desktop Services may not have completed other initialization. When 
   all initialization is complete, Remote Desktop Services calls your 
   <a href="/windows/desktop/api/cchannel/nc-cchannel-channel_init_event_fn">VirtualChannelInitEvent</a> 
   callback function with the <b>CHANNEL_EVENT_INITIALIZED</b> event.

You should not make assumptions about the number of available virtual channels before calling this function, 
   because the system and other plug-ins may have reserved virtual channels. Therefore, you should always check for a 
   <b>CHANNEL_RC_TOO_MANY_CHANNELS</b> return code after calling this function.

When <b>VirtualChannelInit</b> returns, the <b>options</b> member of each 
   <a href="/previous-versions/windows/embedded/aa513856(v=msdn.10)">CHANNEL_DEF</a> structure includes 
   <b>CHANNEL_OPTION_INITIALIZED</b> if the channel was successfully initialized.

The maximum number of channels per client session is <b>CHANNEL_MAX_COUNT</b>.

## -see-also

<a href="/previous-versions/windows/embedded/aa513856(v=msdn.10)">CHANNEL_DEF</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-virtualchannelentry">VirtualChannelEntry</a>



<a href="/windows/desktop/api/cchannel/nc-cchannel-channel_init_event_fn">VirtualChannelInitEvent</a>
