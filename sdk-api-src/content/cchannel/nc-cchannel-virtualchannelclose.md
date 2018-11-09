---
UID: NC:cchannel.VIRTUALCHANNELCLOSE
title: VIRTUALCHANNELCLOSE
author: windows-sdk-content
description: Closes the client end of a virtual channel.
old-location: termserv\virtualchannelclose.htm
tech.root: termserv
ms.assetid: 96fd8910-6cc7-460c-9f63-3363fbbae0b1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: VirtualChannelClose, VirtualChannelClose callback, VirtualChannelClose callback function [Remote Desktop Services], _win32_virtualchannelclose, cchannel/VirtualChannelClose, termserv.virtualchannelclose
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
 - VirtualChannelClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VIRTUALCHANNELCLOSE callback function


## -description


Closes the client end of a virtual channel.

Remote Desktop Services provides a pointer to a 
<b>VirtualChannelClose</b> function in the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380779(v=VS.85).aspx">CHANNEL_ENTRY_POINTS</a> structure passed to your 
<a href="https://msdn.microsoft.com/en-us/library/Aa383560(v=VS.85).aspx">VirtualChannelEntry</a> entry point.


## -parameters




### -param openHandle [in]

Handle to the virtual channel. This is the handle returned in the <i>pOpenHandle</i> parameter of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa383570(v=VS.85).aspx">VirtualChannelOpen</a> function.


## -returns



If the function succeeds, the return value is CHANNEL_RC_OK.

If an error occurs, the function returns one of the following values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa383570(v=VS.85).aspx">VirtualChannelOpen</a>
 

 

