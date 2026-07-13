---
UID: NF:xaudio2.IXAudio2.CreateMasteringVoice
title: IXAudio2::CreateMasteringVoice (xaudio2.h)
description: Creates and configures a mastering voice.
helpviewer_keywords: ["CreateMasteringVoice","CreateMasteringVoice method [XAudio2 Audio Mixing APIs]","CreateMasteringVoice method [XAudio2 Audio Mixing APIs]","IXAudio2 interface","IXAudio2 interface [XAudio2 Audio Mixing APIs]","CreateMasteringVoice method","IXAudio2.CreateMasteringVoice","IXAudio2::CreateMasteringVoice","xaudio2.ixaudio2_interface_createmasteringvoice","xaudio2/IXAudio2::CreateMasteringVoice"]
old-location: xaudio2\ixaudio2_interface_createmasteringvoice.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.CreateMasteringVoice(IXAudio2MasteringVoice@,UINT32,UINT32,UINT32,LPCWSTR,const XAUDIO2_EFFECT_CHAIN,AUDIO_STREAM_CATEGORY)
ms.date: 12/05/2018
ms.keywords: CreateMasteringVoice, CreateMasteringVoice method [XAudio2 Audio Mixing APIs], CreateMasteringVoice method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],CreateMasteringVoice method, IXAudio2.CreateMasteringVoice, IXAudio2::CreateMasteringVoice, xaudio2.ixaudio2_interface_createmasteringvoice, xaudio2/IXAudio2::CreateMasteringVoice
req.header: xaudio2.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2::CreateMasteringVoice
 - xaudio2/IXAudio2::CreateMasteringVoice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2.CreateMasteringVoice
---

# IXAudio2::CreateMasteringVoice


## -description

Creates and configures a mastering voice.

## -parameters

### -param ppMasteringVoice [out]

 If successful, returns a pointer to the new <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice">IXAudio2MasteringVoice</a> object.

### -param X2DEFAULT

TBD

### -param Flags [in]

 Flags that specify the behavior of the mastering voice. This can be 0 or ``XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT``.

### -param InputChannels [in]

Number of channels the mastering voice expects in its input audio. 
<i>InputChannels</i> must be less than or equal to XAUDIO2_MAX_AUDIO_CHANNELS.



You can set <i>InputChannels</i> to XAUDIO2_DEFAULT_CHANNELS, which causes XAudio2 to try to detect the system speaker configuration setup.

### -param InputSampleRate [in]

Sample rate of the input audio data of the mastering voice. This rate must be a multiple of XAUDIO2_QUANTUM_DENOMINATOR. 
<i>InputSampleRate</i> must be between XAUDIO2_MIN_SAMPLE_RATE and XAUDIO2_MAX_SAMPLE_RATE.



You can set <i>InputSampleRate</i> to XAUDIO2_DEFAULT_SAMPLERATE, with the default being determined by the current platform.



Windows XP defaults to 44100.



Windows Vista and Windows 7 default to the setting specified in the Sound Control Panel. The default for this setting is 44100 (or 48000 if required by the driver).

Flags

### -param StreamCategory [in, optional]

The audio stream category to use for this mastering voice.

### -param pEffectChain [in, optional]

Pointer to an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> structure that describes an effect chain to use in the mastering voice, or NULL to use no effects.

### -param szDeviceId [in]

Identifier of the device to receive the output audio. Specifying the default value of NULL causes XAudio2 to select the global default audio device. On Windows 10 or later, NULL will also opt-in to the WASAPI virtualized client unless `XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT` is passed in Flags.

## -returns

Returns S_OK if successful; otherwise, an error code. Returns ERROR_NOT_FOUND if no default audio device exists and NULL is passed in as the szDeviceId parameter. 



See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

Mastering voices receive the output of one or more source or submix voices. They process the data, and send it to the audio output device.



Typically, you should create a mastering voice with an input sample rate that will be used by the majority of the title's audio content. The mastering voice performs a sample rate conversion from this input sample rate to the actual device output rate.



You cannot create a source or submix voices until a mastering voice exists. You cannot destroy a mastering voice if any source or submix voices still exist.



Mastering voices are always processed after all source and submix voices. This means that you need not specify a <i>ProcessingStage</i> parameter to control the processing order.



XAudio2 only allows one mastering voice to exist at once. If you attempt to create more than one voice, XAUDIO2_E_INVALID_CALL is returned. If an additional mastering voice is needed, for example for an output device with a different audio category set, you will need to create an additional XAudio2 instance.



When first created, mastering voices are in the started state.



It is invalid to call <b>CreateMasteringVoice</b> from within a callback (that is, <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> or <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>). If you call <b>CreateMasteringVoice</b> within a callback, it returns XAUDIO2_E_INVALID_CALL.



The <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain">XAUDIO2_EFFECT_CHAIN</a> that is passed in as the pEffectChain argument and any <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor">XAUDIO2_EFFECT_DESCRIPTOR</a> information contained within it are no longer needed after <b>CreateMasteringVoice</b> successfully completes, and may be deleted immediately after <b>CreateMasteringVoice</b> is called.



Note that the DirectX SDK XAUDIO2 version of <b>CreateMasteringVoice</b> took a DeviceIndex argument instead of a szDeviceId and a StreamCategory argument. This reflects the changes needed for the standard Windows device enumeration model.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--build-a-basic-audio-processing-graph">How to: Build a Basic Audio Processing Graph</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a>



<a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>



<a href="/windows/desktop/xaudio2/xaudio2-sample-rate-conversions">XAudio2 Sample Rate Conversions</a>
