---
UID: NC:cchannel.VIRTUALCHANNELCLOSE
title: VIRTUALCHANNELCLOSE
author: windows-driver-content
description: Closes the client end of a virtual channel.
old-location: termserv\virtualchannelclose.htm
old-project: TermServ
ms.assetid: 96fd8910-6cc7-460c-9f63-3363fbbae0b1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: VirtualChannelClose, VirtualChannelClose function pointer [Remote Desktop Services], _win32_virtualchannelclose, cchannel/VirtualChannelClose, termserv.virtualchannelclose
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CEPSetupProperty
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Cchannel.h
api_name:
-	VirtualChannelClose
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# VIRTUALCHANNELCLOSE callback


## -description


Closes the client end of a virtual channel.

Remote Desktop Services provides a pointer to a 
<b>VirtualChannelClose</b> function in the 
<a href="https://msdn.microsoft.com/f64471b0-1f2e-48cb-9f9c-1bb536afc248">CHANNEL_ENTRY_POINTS</a> structure passed to your 
<a href="https://msdn.microsoft.com/1fd185fb-6dc9-4b32-9fa7-15ef76776305">VirtualChannelEntry</a> entry point.


## -parameters




### -param openHandle [in]

Handle to the virtual channel. This is the handle returned in the <i>pOpenHandle</i> parameter of the 
<a href="https://msdn.microsoft.com/4ec75f9d-dbdf-499d-80a9-25fc6e9c5cb9">VirtualChannelOpen</a> function.


## -returns



If the function succeeds, the return value is CHANNEL_RC_OK.

If an error occurs, the function returns one of the following values.




## -see-also




<a href="https://msdn.microsoft.com/4ec75f9d-dbdf-499d-80a9-25fc6e9c5cb9">VirtualChannelOpen</a>
 

 

