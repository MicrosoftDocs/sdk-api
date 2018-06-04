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

# IWTSProtocolConnection::GetProtocolHandles


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetProtocolHandles</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/42f20dfc-e625-4b53-b055-750af4cbd3ec">IWRdsProtocolConnection::GetInputHandles</a> and <a href="https://msdn.microsoft.com/069ee899-ae3a-4043-92b5-e193dbfe4f54">IWRdsProtocolConnection::GetVideoHandle</a>.]

Retrieves keyboard, mouse, sound, and beep handles supported by the protocol.


## -parameters




### -param pKeyboardHandle [out]

A pointer to a keyboard handle. This is a handle to an <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff539967(v=vs.85).aspx">I8042prt keyboard driver</a>.


### -param pMouseHandle [out]

A pointer to a mouse handle. This is a handle to a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff542367(v=vs.85).aspx">Mouclass driver</a>.


### -param pBeepHandle [out]

A pointer to a beep device handle. This handle is not used and must be set to <b>NULL</b>.


### -param pVideoHandle [out]

 A pointer to a video device handle. This is a handle to the video miniport driver for the remote session associated with the protocol.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

