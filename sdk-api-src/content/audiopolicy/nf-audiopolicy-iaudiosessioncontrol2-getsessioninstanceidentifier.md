---
UID: NF:audiopolicy.IAudioSessionControl2.GetSessionInstanceIdentifier
title: IAudioSessionControl2::GetSessionInstanceIdentifier (audiopolicy.h)
description: The GetSessionInstanceIdentifier method retrieves the identifier of the audio session instance.
helpviewer_keywords: ["GetSessionInstanceIdentifier","GetSessionInstanceIdentifier method [Core Audio]","GetSessionInstanceIdentifier method [Core Audio]","IAudioSessionControl2 interface","IAudioSessionControl2 interface [Core Audio]","GetSessionInstanceIdentifier method","IAudioSessionControl2.GetSessionInstanceIdentifier","IAudioSessionControl2::GetSessionInstanceIdentifier","audiopolicy/IAudioSessionControl2::GetSessionInstanceIdentifier","coreaudio.iaudiosessioncontrol2_getsessioninstanceidentifier"]
old-location: coreaudio\iaudiosessioncontrol2_getsessioninstanceidentifier.htm
tech.root: CoreAudio
ms.assetid: 02350812-7f05-400e-87f7-1d912a23050d
ms.date: 12/05/2018
ms.keywords: GetSessionInstanceIdentifier, GetSessionInstanceIdentifier method [Core Audio], GetSessionInstanceIdentifier method [Core Audio],IAudioSessionControl2 interface, IAudioSessionControl2 interface [Core Audio],GetSessionInstanceIdentifier method, IAudioSessionControl2.GetSessionInstanceIdentifier, IAudioSessionControl2::GetSessionInstanceIdentifier, audiopolicy/IAudioSessionControl2::GetSessionInstanceIdentifier, coreaudio.iaudiosessioncontrol2_getsessioninstanceidentifier
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
 - IAudioSessionControl2::GetSessionInstanceIdentifier
 - audiopolicy/IAudioSessionControl2::GetSessionInstanceIdentifier
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
 - IAudioSessionControl2.GetSessionInstanceIdentifier
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
    instances of the application playing, they will have different session instance identifiers. The identifier retrieved by <b>GetSessionInstanceIdentifier</b> is different from the session  identifier, which is shared by all session instances. To get the session  identifier, call <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessionidentifier">IAudioSessionControl2::GetSessionIdentifier</a>.


<b>GetSessionInstanceIdentifier</b> checks whether the session has been disconnected on the default device. It retrieves the identifier string that is cached by the audio client for the device. If the session instance identifier is not found, this method retrieves it from the audio engine. For example code about getting a session instance identifier, see <a href="/windows/desktop/CoreAudio/getting-ducking-events-from-a-communication-device">Getting Ducking Events from a Communication Device</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2">IAudioSessionControl2</a>



<a href="/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>