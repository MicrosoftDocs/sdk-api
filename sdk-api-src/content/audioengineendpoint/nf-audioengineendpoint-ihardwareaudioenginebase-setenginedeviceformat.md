---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.SetEngineDeviceFormat
title: IHardwareAudioEngineBase::SetEngineDeviceFormat
author: windows-sdk-content
description: The SetEngineDeviceFormat method sets the waveform audio format for the hardware audio engine.
old-location: coreaudio\ihardwareaudioenginebase_setenginedeviceformat.htm
tech.root: CoreAudio
ms.assetid: BE4644E7-DBC7-4B30-AD26-483889425195
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IHardwareAudioEngineBase interface [Core Audio],SetEngineDeviceFormat method, IHardwareAudioEngineBase.SetEngineDeviceFormat, IHardwareAudioEngineBase::SetEngineDeviceFormat, SetEngineDeviceFormat, SetEngineDeviceFormat method [Core Audio], SetEngineDeviceFormat method [Core Audio],IHardwareAudioEngineBase interface, audioengineendpoint/IHardwareAudioEngineBase::SetEngineDeviceFormat, coreaudio.ihardwareaudioenginebase_setenginedeviceformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioengineendpoint.h
api_name:
 - IHardwareAudioEngineBase.SetEngineDeviceFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHardwareAudioEngineBase::SetEngineDeviceFormat


## -description


The <b>SetEngineDeviceFormat</b> method sets the waveform audio format for the hardware audio engine.


## -parameters




### -param pDevice [in]

A pointer to an <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interface.


### -param _pwfxFormat [in]

A pointer to a <a href="https://msdn.microsoft.com/f2f050d6-afe2-4647-932b-1287f4538702">WAVEFORMATEX</a> structure that provides information about the hardware audio engine.


## -returns



The <b>SetEngineDeviceFormat</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24">IHardwareAudioEngineBase</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a>
 

 

