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

# SHSendMessageBroadcastA function


## -description


<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Sends a message to all top-level windows in the system.


## -parameters




### -param uMsg [in]

Type: <b>UINT</b>

The message to send.


### -param wParam [in]

Type: <b>WPARAM</b>

Additional message-specific information.


### -param lParam [in]

Type: <b>LPARAM</b>

Additional message-specific information.


## -returns



Type: <b>LRESULT</b>

The return value is not meaningful.




## -remarks



<b>SHSendMessageBroadcast</b> is equivalent to <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a> with <b>HWND_BROADCAST</b>. To avoid causing the Shell to become unresponsive in the case where there could be a window in the system that is not responding to messages, use <b>SHSendMessageBroadcast</b>.

<b>SHSendMessageBroadcast</b> is not exported by name. <b>SHSendMessageBroadcastA</b> is exported from Shlwapi.dll as ordinal 432. <b>SHSendMessageBroadcastW</b> is exported from Shlwapi.dll as ordinal 433.



