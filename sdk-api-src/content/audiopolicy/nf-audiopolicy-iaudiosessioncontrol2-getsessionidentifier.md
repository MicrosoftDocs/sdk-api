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

# IAudioSessionControl2::GetSessionIdentifier


## -description


The <b>GetSessionIdentifier</b> method retrieves the audio session identifier.


## -parameters




### -param pRetVal [out]

Pointer to the address of a null-terminated, wide-character string that  receives the audio session identifier. The string is allocated by this method and must be released by the caller by calling <b>CoTaskMemFree</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.


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
<dt>AUDCLNT_E_DEVICE_INVALIDATED</dt>
</dl>
</td>
<td width="60%">
The audio session is disconnected on the default audio device.

</td>
</tr>
</table>
 




## -remarks



 Each audio session is identified by an identifier string.  This session identifier string is not unique across all instances. If there are two
    instances of the application playing, both instances will have the same session identifier. The identifier retrieved by <b>GetSessionIdentifier</b> is different from the session instance identifier, which is unique across all sessions. To get the session instance identifier, call <a href="https://msdn.microsoft.com/02350812-7f05-400e-87f7-1d912a23050d">IAudioSessionControl2::GetSessionInstanceIdentifier</a>.


<b>GetSessionIdentifier</b> checks whether the session has been disconnected on the default device. It retrieves the identifier string that is cached by the audio client for the device. If the session identifier is not found, this method retrieves it from the audio engine.




## -see-also




<a href="https://msdn.microsoft.com/3bb65edf-103c-4eeb-82b4-7c571cddfcf3">IAudioSessionControl2</a>
 

 

