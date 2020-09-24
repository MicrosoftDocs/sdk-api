---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.SetGfxState
title: IHardwareAudioEngineBase::SetGfxState (audioengineendpoint.h)
description: The SetGfxState method sets the GFX state of the offloaded audio stream.
helpviewer_keywords: ["IHardwareAudioEngineBase interface [Core Audio]","SetGfxState method","IHardwareAudioEngineBase.SetGfxState","IHardwareAudioEngineBase::SetGfxState","SetGfxState","SetGfxState method [Core Audio]","SetGfxState method [Core Audio]","IHardwareAudioEngineBase interface","audioengineendpoint/IHardwareAudioEngineBase::SetGfxState","coreaudio.ihardwareaudioenginebase_setgfxstate"]
old-location: coreaudio\ihardwareaudioenginebase_setgfxstate.htm
tech.root: CoreAudio
ms.assetid: 1B90A629-D41A-4339-918B-DAAF577EB699
ms.date: 12/05/2018
ms.keywords: IHardwareAudioEngineBase interface [Core Audio],SetGfxState method, IHardwareAudioEngineBase.SetGfxState, IHardwareAudioEngineBase::SetGfxState, SetGfxState, SetGfxState method [Core Audio], SetGfxState method [Core Audio],IHardwareAudioEngineBase interface, audioengineendpoint/IHardwareAudioEngineBase::SetGfxState, coreaudio.ihardwareaudioenginebase_setgfxstate
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
 - IHardwareAudioEngineBase::SetGfxState
 - audioengineendpoint/IHardwareAudioEngineBase::SetGfxState
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
 - IHardwareAudioEngineBase.SetGfxState
---

# IHardwareAudioEngineBase::SetGfxState


## -description

The <b>SetGfxState</b> method sets the GFX state of the offloaded audio stream.

## -parameters

### -param pDevice [in]

Pointer to an <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface.

### -param _bEnable [in]

Pointer to a boolean variable.

## -returns

The <b>SetGfxState</b> method returns S_OK to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-ihardwareaudioenginebase">IHardwareAudioEngineBase</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a>