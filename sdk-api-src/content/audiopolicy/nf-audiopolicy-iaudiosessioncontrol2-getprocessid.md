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

# IAudioSessionControl2::GetProcessId


## -description


The <b>GetProcessId</b> method retrieves the process identifier of the audio session.


## -parameters




### -param pRetVal [out]

Pointer to a <b>DWORD</b> variable that receives the process identifier of the audio session. 


## -returns



If the method succeeds, it returns S_OK.
          If it fails, possible return codes include, but are not limited to, the values shown in the following table.


<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>pRetVal</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>AUDCLNT_S_NO_SINGLE_PROCESS</dt>
</dl>
</td>
<td width="60%">
 The session spans more than one process. In this case, <i>pRetVal</i> receives the initial  identifier of the process that created the session. To use this value , include the following definition:

<code>#define AUDCLNT_S_NO_SINGLE_PROCESS            AUDCLNT_SUCCESS (0x00d)</code>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>AUDCLNT_E_DEVICE_INVALIDATED</dt>
</dl>
</td>
<td width="60%">
The audio session is disconnected on the default audio device.

</td>
</tr>
</table>
 




## -remarks



This method overwrites the value that was passed by the application in <i>pRetVal</i>. 

<b>GetProcessId</b> checks whether the audio session has been disconnected on the default device or if the session has switched to another stream. In the case of stream
 switching, this method transfers state information for the new stream to the session. State information includes volume controls, metadata information (display name, icon path), and the session's property store.




## -see-also




<a href="https://msdn.microsoft.com/3bb65edf-103c-4eeb-82b4-7c571cddfcf3">IAudioSessionControl2</a>
 

 

