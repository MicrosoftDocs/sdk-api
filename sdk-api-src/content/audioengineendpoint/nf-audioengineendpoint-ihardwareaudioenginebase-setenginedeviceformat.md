---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.SetEngineDeviceFormat
title: IHardwareAudioEngineBase::SetEngineDeviceFormat (audioengineendpoint.h)
description: The SetEngineDeviceFormat method sets the waveform audio format for the hardware audio engine.
helpviewer_keywords: ["IHardwareAudioEngineBase interface [Core Audio]","SetEngineDeviceFormat method","IHardwareAudioEngineBase.SetEngineDeviceFormat","IHardwareAudioEngineBase::SetEngineDeviceFormat","SetEngineDeviceFormat","SetEngineDeviceFormat method [Core Audio]","SetEngineDeviceFormat method [Core Audio]","IHardwareAudioEngineBase interface","audioengineendpoint/IHardwareAudioEngineBase::SetEngineDeviceFormat","coreaudio.ihardwareaudioenginebase_setenginedeviceformat"]
old-location: coreaudio\ihardwareaudioenginebase_setenginedeviceformat.htm
tech.root: CoreAudio
ms.assetid: BE4644E7-DBC7-4B30-AD26-483889425195
ms.date: 12/05/2018
ms.keywords: IHardwareAudioEngineBase interface [Core Audio],SetEngineDeviceFormat method, IHardwareAudioEngineBase.SetEngineDeviceFormat, IHardwareAudioEngineBase::SetEngineDeviceFormat, SetEngineDeviceFormat, SetEngineDeviceFormat method [Core Audio], SetEngineDeviceFormat method [Core Audio],IHardwareAudioEngineBase interface, audioengineendpoint/IHardwareAudioEngineBase::SetEngineDeviceFormat, coreaudio.ihardwareaudioenginebase_setenginedeviceformat
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
 - IHardwareAudioEngineBase::SetEngineDeviceFormat
 - audioengineendpoint/IHardwareAudioEngineBase::SetEngineDeviceFormat
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
 - IHardwareAudioEngineBase.SetEngineDeviceFormat
---

# IHardwareAudioEngineBase::SetEngineDeviceFormat


## -description

The <b>SetEngineDeviceFormat</b> method sets the waveform audio format for the hardware audio engine.

## -parameters

### -param pDevice [in]

A pointer to an <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface.

### -param _pwfxFormat [in]

A pointer to a <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> structure that provides information about the hardware audio engine.

## -returns

The <b>SetEngineDeviceFormat</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-ihardwareaudioenginebase">IHardwareAudioEngineBase</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a>