---
UID: NF:audiopolicy.IAudioSessionControl2.GetSessionIdentifier
title: IAudioSessionControl2::GetSessionIdentifier (audiopolicy.h)
description: The GetSessionIdentifier method retrieves the audio session identifier.
helpviewer_keywords: ["GetSessionIdentifier","GetSessionIdentifier method [Core Audio]","GetSessionIdentifier method [Core Audio]","IAudioSessionControl2 interface","IAudioSessionControl2 interface [Core Audio]","GetSessionIdentifier method","IAudioSessionControl2.GetSessionIdentifier","IAudioSessionControl2::GetSessionIdentifier","audiopolicy/IAudioSessionControl2::GetSessionIdentifier","coreaudio.iaudiosessioncontrol2_getsessionidentifier"]
old-location: coreaudio\iaudiosessioncontrol2_getsessionidentifier.htm
tech.root: CoreAudio
ms.assetid: 1854e7fe-9d5f-42f3-9c4c-f2a27f26ac17
ms.date: 12/05/2018
ms.keywords: GetSessionIdentifier, GetSessionIdentifier method [Core Audio], GetSessionIdentifier method [Core Audio],IAudioSessionControl2 interface, IAudioSessionControl2 interface [Core Audio],GetSessionIdentifier method, IAudioSessionControl2.GetSessionIdentifier, IAudioSessionControl2::GetSessionIdentifier, audiopolicy/IAudioSessionControl2::GetSessionIdentifier, coreaudio.iaudiosessioncontrol2_getsessionidentifier
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Audiopolicy.idl
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
 - IAudioSessionControl2::GetSessionIdentifier
 - audiopolicy/IAudioSessionControl2::GetSessionIdentifier
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
 - IAudioSessionControl2.GetSessionIdentifier
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
    instances of the application playing, both instances will have the same session identifier. The identifier retrieved by <b>GetSessionIdentifier</b> is different from the session instance identifier, which is unique across all sessions. To get the session instance identifier, call <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier">IAudioSessionControl2::GetSessionInstanceIdentifier</a>.


<b>GetSessionIdentifier</b> checks whether the session has been disconnected on the default device. It retrieves the identifier string that is cached by the audio client for the device. If the session identifier is not found, this method retrieves it from the audio engine.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2">IAudioSessionControl2</a>