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

# MCIWndGetMode macro


## -description



The <b>MCIWndGetMode</b> macro retrieves the current operating mode of an MCI device. MCI devices have several operating modes, which are designated by constants. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/cc327281-434e-4047-9e15-c04a10953f47">MCIWNDM_GETMODE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to the application-defined buffer used to return the mode. 


### -param len

Size, in bytes, of the buffer. 


## -remarks



If the null-terminated string describing the mode is longer than the buffer, it is truncated.

Not all devices can operate in every mode. For example, the MCIAVI device is a playback device; it doesn't support the recording mode. The following modes can be retrieved by using <a href="https://msdn.microsoft.com/cc327281-434e-4047-9e15-c04a10953f47">MCIWNDM_GETMODE</a>:

<table>
<tr>
<th>
              Operating mode
            </th>
<th>
              MCI constant
            </th>
</tr>
<tr>
<td>not ready</td>
<td>MCI_MODE_NOT_READY</td>
</tr>
<tr>
<td>open</td>
<td>MCI_MODE_OPEN</td>
</tr>
<tr>
<td>paused</td>
<td>MCI_MODE_PAUSE</td>
</tr>
<tr>
<td>playing</td>
<td>MCI_MODE_PLAY</td>
</tr>
<tr>
<td>recording</td>
<td>MCI_MODE_RECORD</td>
</tr>
<tr>
<td>seeking</td>
<td>MCI_MODE_SEEK</td>
</tr>
<tr>
<td>stopped</td>
<td>MCI_MODE_STOP</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cc327281-434e-4047-9e15-c04a10953f47">MCIWNDM_GETMODE</a>
 

 

