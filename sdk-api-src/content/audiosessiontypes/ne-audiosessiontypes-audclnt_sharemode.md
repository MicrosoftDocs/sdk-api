---
UID: NE:audiosessiontypes._AUDCLNT_SHAREMODE
title: AUDCLNT_SHAREMODE (audiosessiontypes.h)
description: The AUDCLNT_SHAREMODE enumeration defines constants that indicate whether an audio stream will run in shared mode or in exclusive mode.
helpviewer_keywords: ["AUDCLNT_SHAREMODE","AUDCLNT_SHAREMODE","AUDCLNT_SHAREMODE enumeration [Core Audio]","AUDCLNT_SHAREMODE_EXCLUSIVE","AUDCLNT_SHAREMODE_SHARED","audiosessiontypes/AUDCLNT_SHAREMODE","audiosessiontypes/AUDCLNT_SHAREMODE_EXCLUSIVE","audiosessiontypes/AUDCLNT_SHAREMODE_SHARED","coreaudio.audclnt_sharemode"]
old-location: coreaudio\audclnt_sharemode.htm
tech.root: CoreAudio
ms.assetid: f4870d0f-85d1-48ad-afe0-2f5a960c08fb
ms.date: 12/05/2018
ms.keywords: AUDCLNT_SHAREMODE, AUDCLNT_SHAREMODE , AUDCLNT_SHAREMODE enumeration [Core Audio], AUDCLNT_SHAREMODE_EXCLUSIVE, AUDCLNT_SHAREMODE_SHARED, audiosessiontypes/AUDCLNT_SHAREMODE, audiosessiontypes/AUDCLNT_SHAREMODE_EXCLUSIVE, audiosessiontypes/AUDCLNT_SHAREMODE_SHARED, coreaudio.audclnt_sharemode
req.header: audiosessiontypes.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AUDCLNT_SHAREMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUDCLNT_SHAREMODE
 - audiosessiontypes/_AUDCLNT_SHAREMODE
 - AUDCLNT_SHAREMODE
 - audiosessiontypes/AUDCLNT_SHAREMODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audiosessiontypes.h
api_name:
 - AUDCLNT_SHAREMODE
---

# AUDCLNT_SHAREMODE enumeration


## -description

The <b>AUDCLNT_SHAREMODE</b> enumeration defines constants that indicate whether an audio stream will run in shared mode or in exclusive mode.

## -enum-fields

### -field AUDCLNT_SHAREMODE_SHARED

The audio stream will run in shared mode. For more information, see Remarks.

### -field AUDCLNT_SHAREMODE_EXCLUSIVE

The audio stream will run in exclusive mode. For more information, see Remarks.

## -remarks

The <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> and <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-isformatsupported">IAudioClient::IsFormatSupported</a> methods use the constants defined in the <b>AUDCLNT_SHAREMODE</b> enumeration.

In shared mode, the client can share the audio endpoint device with clients that run in other user-mode processes. The audio engine always supports formats for client streams that match the engine's mix format. In addition, the audio engine might support another format if the Windows audio service can insert system effects into the client stream to convert the client format to the mix format.

In exclusive mode, the Windows audio service attempts to establish a connection in which the client has exclusive access to the audio endpoint device. In this mode, the audio engine inserts no system effects into the local stream to aid in the creation of the connection point. Either the audio device can handle the specified format directly or the method fails.

For more information about shared-mode and exclusive-mode streams, see <a href="/windows/desktop/CoreAudio/user-mode-audio-components">User-Mode Audio Components</a>.

Starting with Xbox May 2021 Update, you can open an audio client in exclusive mode on Xbox.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-constants">Core Audio Constants</a>



<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-isformatsupported">IAudioClient::IsFormatSupported</a>