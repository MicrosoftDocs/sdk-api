---
UID: NF:xaudio2.IXAudio2.CreateMasteringVoice
title: IXAudio2::CreateMasteringVoice
author: windows-sdk-content
description: Creates and configures a mastering voice.
old-location: xaudio2\ixaudio2_interface_createmasteringvoice.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.CreateMasteringVoice(IXAudio2MasteringVoice@,UINT32,UINT32,UINT32,LPCWSTR,const XAUDIO2_EFFECT_CHAIN,AUDIO_STREAM_CATEGORY)
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: CreateMasteringVoice, CreateMasteringVoice method [XAudio2 Audio Mixing APIs], CreateMasteringVoice method [XAudio2 Audio Mixing APIs],IXAudio2 interface, IXAudio2 interface [XAudio2 Audio Mixing APIs],CreateMasteringVoice method, IXAudio2.CreateMasteringVoice, IXAudio2::CreateMasteringVoice, xaudio2.ixaudio2_interface_createmasteringvoice, xaudio2/IXAudio2::CreateMasteringVoice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2.CreateMasteringVoice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2::CreateMasteringVoice


## -description


Creates and configures a mastering voice.


## -parameters




### -param ppMasteringVoice [out]

 If successful, returns a pointer to the new <a href="https://msdn.microsoft.com/library/Ee415912(v=VS.85).aspx">IXAudio2MasteringVoice</a> object.


### -param X2DEFAULT






#### - Flags [in]

 Flags that specify the behavior of the mastering voice. Must be 0.


#### - InputChannels [in]

Number of channels the mastering voice expects in its input audio. 
<i>InputChannels</i> must be less than or equal to XAUDIO2_MAX_AUDIO_CHANNELS.



You can set <i>InputChannels</i> to XAUDIO2_DEFAULT_CHANNELS, which causes XAudio2 to try to detect the system speaker configuration setup.




#### - InputSampleRate [in]

Sample rate of the input audio data of the mastering voice. This rate must be a multiple of XAUDIO2_QUANTUM_DENOMINATOR. 
<i>InputSampleRate</i> must be between XAUDIO2_MIN_SAMPLE_RATE and XAUDIO2_MAX_SAMPLE_RATE.



You can set <i>InputSampleRate</i> to XAUDIO2_DEFAULT_SAMPLERATE, with the default being determined by the current platform.



Windows XP defaults to 44100.



Windows Vista and Windows 7 default to the setting specified in the Sound Control Panel. The default for this setting is 44100 (or 48000 if required by the driver).

Flags



#### - StreamCategory [in, optional]

The audio stream category to use for this mastering voice.


#### - pEffectChain [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/library/Ee419235(v=VS.85).aspx">XAUDIO2_EFFECT_CHAIN</a> structure that describes an effect chain to use in the mastering voice, or NULL to use no effects.


#### - szDeviceId [in]

Identifier of the device to receive the output audio. Specifying the default value of NULL causes XAudio2 to select the global default audio device.


## -returns



Returns S_OK if successful; otherwise, an error code. Returns ERROR_NOT_FOUND if no default audio device exists and NULL is passed in as the szDeviceId parameter. 



See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.






## -remarks



Mastering voices receive the output of one or more source or submix voices. They process the data, and send it to the audio output device.



Typically, you should create a mastering voice with an input sample rate that will be used by the majority of the title's audio content. The mastering voice performs a sample rate conversion from this input sample rate to the actual device output rate.



You cannot create a source or submix voices until a mastering voice exists. You cannot destroy a mastering voice if any source or submix voices still exist.



Mastering voices are always processed after all source and submix voices. This means that you need not specify a <i>ProcessingStage</i> parameter to control the processing order.



XAudio2 only allows one mastering voice to exist at once. If you attempt to create more than one voice, XAUDIO2_E_INVALID_CALL is returned. If an additional mastering voice is needed, for example for an output device with a different audio category set, you will need to create an additional XAudio2 instance.



When first created, mastering voices are in the started state.



It is invalid to call <b>CreateMasteringVoice</b> from within a callback (that is, <a href="https://msdn.microsoft.com/library/Ee415910(v=VS.85).aspx">IXAudio2EngineCallback</a> or <a href="https://msdn.microsoft.com/library/Ee415919(v=VS.85).aspx">IXAudio2VoiceCallback</a>). If you call <b>CreateMasteringVoice</b> within a callback, it returns XAUDIO2_E_INVALID_CALL.



The <a href="https://msdn.microsoft.com/library/Ee419235(v=VS.85).aspx">XAUDIO2_EFFECT_CHAIN</a> that is passed in as the pEffectChain argument and any <a href="https://msdn.microsoft.com/library/Ee419236(v=VS.85).aspx">XAUDIO2_EFFECT_DESCRIPTOR</a> information contained within it are no longer needed after <b>CreateMasteringVoice</b> successfully completes, and may be deleted immediately after <b>CreateMasteringVoice</b> is called.



Note that the DirectX SDK XAUDIO2 version of <b>CreateMasteringVoice</b> took a DeviceIndex argument instead of a szDeviceId and a StreamCategory argument. This reflects the changes needed for the standard Windows device enumeration model.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/40f79959-23c9-4513-363b-2f2fc85e4c0a">How to: Build a Basic Audio Processing Graph</a>



<a href="https://msdn.microsoft.com/library/Ee415908(v=VS.85).aspx">IXAudio2</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>



<a href="https://msdn.microsoft.com/be34ce62-6552-45e2-a247-830ab55ea9ec">XAudio2 Sample Rate Conversions</a>
 

 

