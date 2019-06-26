---
UID: NC:cchannel.VIRTUALCHANNELENTRY
title: VIRTUALCHANNELENTRY (cchannel.h)
author: windows-sdk-content
description: An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.
old-location: termserv\virtualchannelentry.htm
tech.root: TermServ
ms.assetid: 1fd185fb-6dc9-4b32-9fa7-15ef76776305
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VirtualChannelEntry, VirtualChannelEntry callback, VirtualChannelEntry callback function [Remote Desktop Services], _win32_virtualchannelentry, cchannel/VirtualChannelEntry, termserv.virtualchannelentry
ms.topic: callback
f1_keywords: 
 - "cchannel/VirtualChannelEntry"
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
 - VirtualChannelEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VIRTUALCHANNELENTRY callback function


## -description


An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels. Remote Desktop Services calls this entry point to pass a set of function pointers to the client DLL. The client calls these functions to work with virtual channels. Your 
<b>VirtualChannelEntry</b> implementation must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a> function to initialize access to virtual channels.


## -parameters




### -param pEntryPoints [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/ns-cchannel-tagchannel_entry_points">CHANNEL_ENTRY_POINTS</a> structure that contains pointers to the client-side virtual channel functions.

This pointer is no longer valid after the 
<b>VirtualChannelEntry</b> function returns. You must make a copy of this structure in extension-allocated memory for later use.


## -returns



Return <b>TRUE</b> if the function is successful.

Return <b>FALSE</b> if an error occurs. In this case, Remote Desktop Services unloads your DLL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/ns-cchannel-tagchannel_entry_points">CHANNEL_ENTRY_POINTS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cchannel/nc-cchannel-virtualchannelinit">VirtualChannelInit</a>
 

 

