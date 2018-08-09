---
UID: NF:audiopolicy.IAudioSessionControl.GetDisplayName
title: IAudioSessionControl::GetDisplayName
author: windows-sdk-content
description: The GetDisplayName method retrieves the display name for the audio session.
old-location: coreaudio\iaudiosessioncontrol_getdisplayname.htm
old-project: CoreAudio
ms.assetid: 28493e3a-ee5a-4331-b5b5-ba0bf2ee3370
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetDisplayName, GetDisplayName method [Core Audio], GetDisplayName method [Core Audio],IAudioSessionControl interface, IAudioSessionControl interface [Core Audio],GetDisplayName method, IAudioSessionControl.GetDisplayName, IAudioSessionControl::GetDisplayName, IAudioSessionControlGetDisplayName, audiopolicy/IAudioSessionControl::GetDisplayName, coreaudio.iaudiosessioncontrol_getdisplayname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Audiopolicy.h
api_name:
 - IAudioSessionControl.GetDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionControl::GetDisplayName


## -description



The <b>GetDisplayName</b> method retrieves the display name for the audio session.




## -parameters




### -param pRetVal [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string that contains the display name. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pRetVal</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -remarks



If the client has not called <a href="https://msdn.microsoft.com/d12c12ed-a556-4743-952e-2eb4f58ee0eb">IAudioSessionControl::SetDisplayName</a> to set the display name, the string will be empty. Rather than display an empty name string, the Sndvol program uses a default, automatically generated name to label the volume control for the audio session.




## -see-also




<a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl Interface</a>



<a href="https://msdn.microsoft.com/d12c12ed-a556-4743-952e-2eb4f58ee0eb">IAudioSessionControl::SetDisplayName</a>
 

 

