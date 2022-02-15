---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount
title: IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount (audioengineendpoint.h)
description: The GetAvailableOffloadConnectorCount method retrieves the number of available endpoints that can handle offloaded streams on the hardware audio engine.
helpviewer_keywords: ["GetAvailableOffloadConnectorCount","GetAvailableOffloadConnectorCount method [Core Audio]","GetAvailableOffloadConnectorCount method [Core Audio]","IHardwareAudioEngineBase interface","IHardwareAudioEngineBase interface [Core Audio]","GetAvailableOffloadConnectorCount method","IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount","IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount","audioengineendpoint/IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount","coreaudio.ihardwareaudioenginebase_getavailableoffloadconnectorcount"]
old-location: coreaudio\ihardwareaudioenginebase_getavailableoffloadconnectorcount.htm
tech.root: CoreAudio
ms.assetid: FCAFF20A-812A-4232-A86C-79D07D5AE26F
ms.date: 12/05/2018
ms.keywords: GetAvailableOffloadConnectorCount, GetAvailableOffloadConnectorCount method [Core Audio], GetAvailableOffloadConnectorCount method [Core Audio],IHardwareAudioEngineBase interface, IHardwareAudioEngineBase interface [Core Audio],GetAvailableOffloadConnectorCount method, IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount, IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount, audioengineendpoint/IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount, coreaudio.ihardwareaudioenginebase_getavailableoffloadconnectorcount
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount
 - audioengineendpoint/IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount
---

# IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount


## -description

The <b>GetAvailableOffloadConnectorCount</b> method retrieves the number of available endpoints that can handle offloaded streams on the hardware audio engine.

## -parameters

### -param _pwstrDeviceId [in]

A pointer to the device ID of the hardware audio engine device.

### -param _uConnectorId [in]

The identifier for the endpoint connector.

### -param _pAvailableConnectorInstanceCount [out]

A pointer to the number of available endpoint connectors that can handle offloaded audio streams.

## -returns

The <b>GetAvailableOffloadConnectorCount</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-ihardwareaudioenginebase">IHardwareAudioEngineBase</a>