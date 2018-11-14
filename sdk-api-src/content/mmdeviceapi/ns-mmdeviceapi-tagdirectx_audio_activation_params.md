---
UID: NS:mmdeviceapi.tagDIRECTX_AUDIO_ACTIVATION_PARAMS
title: tagDIRECTX_AUDIO_ACTIVATION_PARAMS
author: windows-sdk-content
description: The DIRECTX_AUDIO_ACTIVATION_PARAMS structure specifies the initialization parameters for a DirectSound stream.
old-location: coreaudio\directx_audio_activation_params.htm
tech.root: CoreAudio
ms.assetid: d8d16c1c-5306-42a7-885b-4e1c5ee7634d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PDIRECTX_AUDIO_ACTIVATION_PARAMS, DIRECTX_AUDIO_ACTIVATION_PARAMS, DIRECTX_AUDIO_ACTIVATION_PARAMS structure [Core Audio], PDIRECTX_AUDIO_ACTIVATION_PARAMS, PDIRECTX_AUDIO_ACTIVATION_PARAMS structure pointer [Core Audio], coreaudio.directx_audio_activation_params, mmdeviceapi/DIRECTX_AUDIO_ACTIVATION_PARAMS, mmdeviceapi/PDIRECTX_AUDIO_ACTIVATION_PARAMS, tagDIRECTX_AUDIO_ACTIVATION_PARAMS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmdeviceapi.h
api_name:
 - DIRECTX_AUDIO_ACTIVATION_PARAMS
product: Windows
targetos: Windows
req.typenames: DIRECTX_AUDIO_ACTIVATION_PARAMS, *PDIRECTX_AUDIO_ACTIVATION_PARAMS
req.redist: 
---

# tagDIRECTX_AUDIO_ACTIVATION_PARAMS structure


## -description



The <b>DIRECTX_AUDIO_ACTIVATION_PARAMS</b> structure specifies the initialization parameters for a DirectSound stream.




## -struct-fields




### -field cbDirectXAudioActivationParams

The size, in bytes, of the <b>DIRECTX_AUDIO_ACTIVATION_PARAMS</b> structure. Set this member to sizeof(DIRECTX_AUDIO_ACTIVATION_PARAMS).


### -field guidAudioSession

Session GUID. This member is a GUID value that identifies the audio session that the stream belongs to. If the GUID identifies a session that has been previously opened, the method adds the stream to that session. If the GUID does not identify an existing session, the method opens a new session and adds the stream to that session. The stream remains a member of the same session for its lifetime.


### -field dwAudioStreamFlags

Stream-initialization flags. This member specifies whether the stream belongs to a cross-process session or to a session that is specific to the current process. Set this member to 0 or to the following <a href="https://msdn.microsoft.com/7b2267c3-79f5-4ada-a7ce-78dd514f8487">AUDCLNT_STREAMFLAGS_XXX</a> constant:

AUDCLNT_STREAMFLAGS_CROSSPROCESS


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a> method. When activating an <b>IDirectSound</b>, <b>IDirectSoundCapture</b>, or <b>IBaseFilter</b> interface on an audio endpoint device, the <b>DIRECTX_AUDIO_ACTIVATION_PARAMS</b> structure specifies the session GUID and stream-initialization flags for the audio stream that the DirectSound module creates and encapsulates in the interface instance. During the <b>Activate</b> call, DirectSound calls the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method and specifies the session GUID and stream-initialization flags from the <b>DIRECTX_AUDIO_ACTIVATION_PARAMS</b> structure as input parameters.

For more information about <b>IDirectSound</b>, <b>IDirectSoundCapture</b>, and <b>IBaseFilter</b>, see the Windows SDK documentation.

For a code example that uses the <b>DIRECTX_AUDIO_ACTIVATION_PARAMS</b> structure, see <a href="https://msdn.microsoft.com/54f42bda-b4a0-465c-9ce6-9102d2908776">Device Roles for DirectShow Applications</a>. 




## -see-also




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>
 

 

