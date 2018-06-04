---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# VIRTUALCHANNELENTRY callback function


## -description



    An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels. Remote Desktop Services calls this entry point to pass a set of function pointers to the client DLL. The client calls these functions to work with virtual channels. Your 
<b>VirtualChannelEntry</b> implementation must call the 
<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a> function to initialize access to virtual channels.


## -parameters




### -param pEntryPoints [in]

Pointer to a 
<a href="https://msdn.microsoft.com/f64471b0-1f2e-48cb-9f9c-1bb536afc248">CHANNEL_ENTRY_POINTS</a> structure that contains pointers to the client-side virtual channel functions.

This pointer is no longer valid after the 
<b>VirtualChannelEntry</b> function returns. You must make a copy of this structure in extension-allocated memory for later use.


## -returns



Return <b>TRUE</b> if the function is successful.

Return <b>FALSE</b> if an error occurs. In this case, Remote Desktop Services unloads your DLL.




## -see-also




<a href="https://msdn.microsoft.com/f64471b0-1f2e-48cb-9f9c-1bb536afc248">CHANNEL_ENTRY_POINTS</a>



<a href="https://msdn.microsoft.com/3dae59dc-e70f-450e-a324-a4d68341a72e">VirtualChannelInit</a>
 

 

