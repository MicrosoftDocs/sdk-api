---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount
title: IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount
author: windows-sdk-content
description: The GetAvailableOffloadConnectorCount method retrieves the number of avaialable endpoints that can handle offloaded streams on the hardware audio engine.
old-location: coreaudio\ihardwareaudioenginebase_getavailableoffloadconnectorcount.htm
old-project: CoreAudio
ms.assetid: FCAFF20A-812A-4232-A86C-79D07D5AE26F
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetAvailableOffloadConnectorCount, GetAvailableOffloadConnectorCount method [Core Audio], GetAvailableOffloadConnectorCount method [Core Audio],IHardwareAudioEngineBase interface, IHardwareAudioEngineBase interface [Core Audio],GetAvailableOffloadConnectorCount method, IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount, IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount, audioengineendpoint/IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount, coreaudio.ihardwareaudioenginebase_getavailableoffloadconnectorcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audioengineendpoint.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IHardwareAudioEngineBase.GetAvailableOffloadConnectorCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount


## -description


The <b>GetAvailableOffloadConnectorCount</b> method retrieves the number of avaialable endpoints that can handle offloaded streams on the hardware audio engine.


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




<a href="https://msdn.microsoft.com/6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24">IHardwareAudioEngineBase</a>
 

 

