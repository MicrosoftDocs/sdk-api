---
UID: NF:audiopolicy.IAudioSessionControl2.GetProcessId
title: IAudioSessionControl2::GetProcessId (audiopolicy.h)
description: The GetProcessId method retrieves the process identifier of the audio session.
helpviewer_keywords: ["GetProcessId","GetProcessId method [Core Audio]","GetProcessId method [Core Audio]","IAudioSessionControl2 interface","IAudioSessionControl2 interface [Core Audio]","GetProcessId method","IAudioSessionControl2.GetProcessId","IAudioSessionControl2::GetProcessId","audiopolicy/IAudioSessionControl2::GetProcessId","coreaudio.iaudiosessioncontrol2_getprocessid"]
old-location: coreaudio\iaudiosessioncontrol2_getprocessid.htm
tech.root: CoreAudio
ms.assetid: 17ae85ad-e2ef-4a87-9d0f-58baa080ff98
ms.date: 12/05/2018
ms.keywords: GetProcessId, GetProcessId method [Core Audio], GetProcessId method [Core Audio],IAudioSessionControl2 interface, IAudioSessionControl2 interface [Core Audio],GetProcessId method, IAudioSessionControl2.GetProcessId, IAudioSessionControl2::GetProcessId, audiopolicy/IAudioSessionControl2::GetProcessId, coreaudio.iaudiosessioncontrol2_getprocessid
req.header: audiopolicy.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioSessionControl2::GetProcessId
 - audiopolicy/IAudioSessionControl2::GetProcessId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionControl2.GetProcessId
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

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2">IAudioSessionControl2</a>