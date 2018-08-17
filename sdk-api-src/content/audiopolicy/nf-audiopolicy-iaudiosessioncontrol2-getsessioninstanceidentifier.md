---
UID: NF:audiopolicy.IAudioSessionControl2.GetSessionInstanceIdentifier
title: IAudioSessionControl2::GetSessionInstanceIdentifier
author: windows-sdk-content
description: The GetSessionInstanceIdentifier method retrieves the identifier of the audio session instance.
old-location: coreaudio\iaudiosessioncontrol2_getsessioninstanceidentifier.htm
old-project: CoreAudio
ms.assetid: 02350812-7f05-400e-87f7-1d912a23050d
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetSessionInstanceIdentifier, GetSessionInstanceIdentifier method [Core Audio], GetSessionInstanceIdentifier method [Core Audio],IAudioSessionControl2 interface, IAudioSessionControl2 interface [Core Audio],GetSessionInstanceIdentifier method, IAudioSessionControl2.GetSessionInstanceIdentifier, IAudioSessionControl2::GetSessionInstanceIdentifier, audiopolicy/IAudioSessionControl2::GetSessionInstanceIdentifier, coreaudio.iaudiosessioncontrol2_getsessioninstanceidentifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audiopolicy.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionControl2.GetSessionInstanceIdentifier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionControl2::GetSessionInstanceIdentifier


## -description


The <b>GetSessionInstanceIdentifier</b> method retrieves the identifier of the audio session instance.


## -parameters




### -param pRetVal [out]

Pointer to the address of a null-terminated, wide-character string that receives the identifier of a particular instance of the audio session. The string is allocated by this method and must be released by the caller by calling <b>CoTaskMemFree</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.


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



 Each audio session instance is identified by a unique string.  This  string represents a particular instance of the audio session and, unlike the session identifier, is unique across all instances. If there are two
    instances of the application playing, they will have different session instance identifiers. The identifier retrieved by <b>GetSessionInstanceIdentifier</b> is different from the session  identifier, which is shared by all session instances. To get the session  identifier, call <a href="https://msdn.microsoft.com/1854e7fe-9d5f-42f3-9c4c-f2a27f26ac17">IAudioSessionControl2::GetSessionIdentifier</a>.


<b>GetSessionInstanceIdentifier</b> checks whether the session has been disconnected on the default device. It retrieves the identifier string that is cached by the audio client for the device. If the session instance identifier is not found, this method retrieves it from the audio engine. For example code about getting a session instance identifier, see <a href="https://msdn.microsoft.com/709ad912-6b03-4ad3-bc47-ad8b6bd6de45">Getting Ducking Events from a Communication Device</a>.




## -see-also




<a href="https://msdn.microsoft.com/3bb65edf-103c-4eeb-82b4-7c571cddfcf3">IAudioSessionControl2</a>



<a href="https://msdn.microsoft.com/bec2127d-fb82-436d-beee-d43e8fef5c35">Using a Communication Device</a>
 

 

