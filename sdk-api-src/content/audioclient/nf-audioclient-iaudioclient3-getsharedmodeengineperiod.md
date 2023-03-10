---
UID: NF:audioclient.IAudioClient3.GetSharedModeEnginePeriod
title: IAudioClient3::GetSharedModeEnginePeriod (audioclient.h)
description: Returns the range of periodicities supported by the engine for the specified stream format.
helpviewer_keywords: ["GetSharedModeEnginePeriod","GetSharedModeEnginePeriod method [Core Audio]","GetSharedModeEnginePeriod method [Core Audio]","IAudioClient3 interface","IAudioClient3 interface [Core Audio]","GetSharedModeEnginePeriod method","IAudioClient3.GetSharedModeEnginePeriod","IAudioClient3::GetSharedModeEnginePeriod","audioclient/IAudioClient3::GetSharedModeEnginePeriod","coreaudio.iaudioclient3_getsharedmodeengineperiod"]
old-location: coreaudio\iaudioclient3_getsharedmodeengineperiod.htm
tech.root: CoreAudio
ms.assetid: 41ED045F-0C47-40BE-9ECD-6A925E166E6D
ms.date: 12/05/2018
ms.keywords: GetSharedModeEnginePeriod, GetSharedModeEnginePeriod method [Core Audio], GetSharedModeEnginePeriod method [Core Audio],IAudioClient3 interface, IAudioClient3 interface [Core Audio],GetSharedModeEnginePeriod method, IAudioClient3.GetSharedModeEnginePeriod, IAudioClient3::GetSharedModeEnginePeriod, audioclient/IAudioClient3::GetSharedModeEnginePeriod, coreaudio.iaudioclient3_getsharedmodeengineperiod
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IAudioClient3::GetSharedModeEnginePeriod
 - audioclient/IAudioClient3::GetSharedModeEnginePeriod
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClient3.GetSharedModeEnginePeriod
---

# IAudioClient3::GetSharedModeEnginePeriod


## -description

Returns the range of periodicities supported by the engine for the specified stream format. The periodicity of the engine is the rate at which the engine wakes an event-driven audio client
    to transfer audio data to or from the engine.
    The values returned depend on the characteristics of the audio client as specified through a previous call to 
    <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient2-setclientproperties">IAudioClient2::SetClientProperties</a>.

## -parameters

### -param pFormat [in]

Type: <b>const <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>*</b>

The stream format for which the supported periodicities are queried.

### -param pDefaultPeriodInFrames [out]

Type: <b>UINT32*</b>

The default period with which the engine will wake the client for 
    transferring audio samples

### -param pFundamentalPeriodInFrames [out]

Type: <b>UINT32*</b>

The fundamental period with which the engine will wake the client for 
    transferring audio samples. When setting the audio engine periodicity, you must use an integral multiple of this value.

### -param pMinPeriodInFrames [out]

Type: <b>UINT32*</b>

The shortest period, in audio frames, with which the audio engine will wake the client for 
    transferring audio samples.

### -param pMaxPeriodInFrames [out]

Type: <b>UINT32*</b>

The longest period, in audio frames,  with which the audio engine will wake the client for 
    transferring audio samples.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -remarks

Audio clients request a specific periodicity from the audio engine with the <i>PeriodInFrames</i> parameter to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient3-initializesharedaudiostream">IAudioClient3::InitializeSharedAudioStream</a>. The value of <i>PeriodInFrames</i> must be an integral multiple of the value returned in the <i>pFundamentalPeriodInFrames</i> parameter.  <i>PeriodInFrames</i> must also be greater than or equal to the value returned in <i>pMinPeriodInFrames</i> and less than or equal to the value of <i>pMaxPeriodInFrames</i>.

For example, for a 44100 kHz format, <b>GetSharedModeEnginePeriod</b> might return:







* <i>pDefaultPeriodInFrames</i> = 448 frames (about 10.16 milliseconds)

* <i>pFundamentalPeriodInFrames</i> = 4 frames (about 0.09 milliseconds)

* <i>pMinPeriodInFrames</i> = 48 frames (about 1.09 milliseconds)

* <i>pMaxPeriodInFrames</i> = 448 frames (same as the default)

Allowed values for the <i>PeriodInFrames</i> parameter to <b>InitializeSharedAudioStream</b> would include 48 and 448. They would also include things like 96 and 128.

They would NOT include 4 (which is smaller than the minimum allowed value) or 98 (which is not a multiple of the fundamental) or 1000 (which is larger than the maximum allowed value).

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient3">IAudioClient3</a>