---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.GetEngineFormat
title: IHardwareAudioEngineBase::GetEngineFormat
author: windows-sdk-content
description: The GetEngineFormat method retrieves the current data format of the offloaded audio stream.
old-location: coreaudio\ihardwareaudioenginebase_getengineformat.htm
old-project: CoreAudio
ms.assetid: 150F8E7C-35A0-42DA-8E3D-69835153382F
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetEngineFormat, GetEngineFormat method [Core Audio], GetEngineFormat method [Core Audio],IHardwareAudioEngineBase interface, IHardwareAudioEngineBase interface [Core Audio],GetEngineFormat method, IHardwareAudioEngineBase.GetEngineFormat, IHardwareAudioEngineBase::GetEngineFormat, audioengineendpoint/IHardwareAudioEngineBase::GetEngineFormat, coreaudio.ihardwareaudioenginebase_getengineformat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioengineendpoint.h
api_name:
 - IHardwareAudioEngineBase.GetEngineFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IHardwareAudioEngineBase::GetEngineFormat


## -description


The <b>GetEngineFormat</b> method retrieves the current data format of the offloaded audio stream.


## -parameters




### -param pDevice [in]

A pointer to an <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interface.


### -param _bRequestDeviceFormat [in]

A Boolean variable that indicates whether or not the <b>IMMDevice</b> interface is being accessed to retrieve the device format.


### -param _ppwfxFormat [out]

A pointer to a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that provides information about the hardware audio engine. This includes the waveform audio format type, the number of audio channels, and the sample rate of the audio engine. 


## -returns



The <b>GetEngineFormat</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24">IHardwareAudioEngineBase</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>
 

 

