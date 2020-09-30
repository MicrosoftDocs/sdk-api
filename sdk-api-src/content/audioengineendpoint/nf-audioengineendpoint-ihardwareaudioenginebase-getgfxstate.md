---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.GetGfxState
title: IHardwareAudioEngineBase::GetGfxState (audioengineendpoint.h)
description: The GetGfxState method retrieves the GFX state of the offloaded audio stream.
helpviewer_keywords: ["GetGfxState","GetGfxState method [Core Audio]","GetGfxState method [Core Audio]","IHardwareAudioEngineBase interface","IHardwareAudioEngineBase interface [Core Audio]","GetGfxState method","IHardwareAudioEngineBase.GetGfxState","IHardwareAudioEngineBase::GetGfxState","audioengineendpoint/IHardwareAudioEngineBase::GetGfxState","coreaudio.ihardwareaudioenginebase_getgfxstate"]
old-location: coreaudio\ihardwareaudioenginebase_getgfxstate.htm
tech.root: CoreAudio
ms.assetid: 519D3BF1-B5C3-469A-A188-7D741E288337
ms.date: 12/05/2018
ms.keywords: GetGfxState, GetGfxState method [Core Audio], GetGfxState method [Core Audio],IHardwareAudioEngineBase interface, IHardwareAudioEngineBase interface [Core Audio],GetGfxState method, IHardwareAudioEngineBase.GetGfxState, IHardwareAudioEngineBase::GetGfxState, audioengineendpoint/IHardwareAudioEngineBase::GetGfxState, coreaudio.ihardwareaudioenginebase_getgfxstate
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
 - IHardwareAudioEngineBase::GetGfxState
 - audioengineendpoint/IHardwareAudioEngineBase::GetGfxState
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
 - IHardwareAudioEngineBase.GetGfxState
---

# IHardwareAudioEngineBase::GetGfxState


## -description

The <b>GetGfxState</b> method retrieves the GFX state of the offloaded audio stream.

## -parameters

### -param pDevice [in]

Pointer to an <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface.

### -param _pbEnable [out]

Pointer to a boolean variable.

## -returns

The <b>GetGfxState</b> method returns S_OK to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-ihardwareaudioenginebase">IHardwareAudioEngineBase</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a>