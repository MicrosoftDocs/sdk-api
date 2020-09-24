---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.GetEngineFormat
title: IHardwareAudioEngineBase::GetEngineFormat (audioengineendpoint.h)
description: The GetEngineFormat method retrieves the current data format of the offloaded audio stream.
helpviewer_keywords: ["GetEngineFormat","GetEngineFormat method [Core Audio]","GetEngineFormat method [Core Audio]","IHardwareAudioEngineBase interface","IHardwareAudioEngineBase interface [Core Audio]","GetEngineFormat method","IHardwareAudioEngineBase.GetEngineFormat","IHardwareAudioEngineBase::GetEngineFormat","audioengineendpoint/IHardwareAudioEngineBase::GetEngineFormat","coreaudio.ihardwareaudioenginebase_getengineformat"]
old-location: coreaudio\ihardwareaudioenginebase_getengineformat.htm
tech.root: CoreAudio
ms.assetid: 150F8E7C-35A0-42DA-8E3D-69835153382F
ms.date: 12/05/2018
ms.keywords: GetEngineFormat, GetEngineFormat method [Core Audio], GetEngineFormat method [Core Audio],IHardwareAudioEngineBase interface, IHardwareAudioEngineBase interface [Core Audio],GetEngineFormat method, IHardwareAudioEngineBase.GetEngineFormat, IHardwareAudioEngineBase::GetEngineFormat, audioengineendpoint/IHardwareAudioEngineBase::GetEngineFormat, coreaudio.ihardwareaudioenginebase_getengineformat
req.header: audioengineendpoint.h
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
 - IHardwareAudioEngineBase::GetEngineFormat
 - audioengineendpoint/IHardwareAudioEngineBase::GetEngineFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioengineendpoint.h
api_name:
 - IHardwareAudioEngineBase.GetEngineFormat
---

# IHardwareAudioEngineBase::GetEngineFormat


## -description

The <b>GetEngineFormat</b> method retrieves the current data format of the offloaded audio stream.

## -parameters

### -param pDevice [in]

A pointer to an <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface.

### -param _bRequestDeviceFormat [in]

A Boolean variable that indicates whether or not the <b>IMMDevice</b> interface is being accessed to retrieve the device format.

### -param _ppwfxFormat [out]

A pointer to a pointer to a <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> structure that provides information about the hardware audio engine. This includes the waveform audio format type, the number of audio channels, and the sample rate of the audio engine.

## -returns

The <b>GetEngineFormat</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-ihardwareaudioenginebase">IHardwareAudioEngineBase</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a>



<a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a>