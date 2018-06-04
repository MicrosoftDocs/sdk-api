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

# IWTSProtocolConnection::SendBeep


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::SendBeep</b> is no longer available for use as of Windows Server 2012.]

Sends a sound pulse to the console speaker on the client.

The beep() function does not cause <b>SendBeep</b> to be called. To work around this issue, the user must enable Remote Desktop Services audio redirection capabilities to remotely hear beep sounds.


## -parameters




### -param Frequency [in]

An integer that contains the pulse frequency ranging from 37 to 32,767 Hertz.


### -param Duration [in]

An integer that contains the pulse duration, in milliseconds.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

