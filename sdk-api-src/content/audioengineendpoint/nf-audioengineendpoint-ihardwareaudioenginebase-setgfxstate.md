---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.SetGfxState
title: IHardwareAudioEngineBase::SetGfxState
author: windows-sdk-content
description: The SetGfxState method sets the GFX state of the offloaded audio stream.
old-location: coreaudio\ihardwareaudioenginebase_setgfxstate.htm
tech.root: CoreAudio
ms.assetid: 1B90A629-D41A-4339-918B-DAAF577EB699
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IHardwareAudioEngineBase interface [Core Audio],SetGfxState method, IHardwareAudioEngineBase.SetGfxState, IHardwareAudioEngineBase::SetGfxState, SetGfxState, SetGfxState method [Core Audio], SetGfxState method [Core Audio],IHardwareAudioEngineBase interface, audioengineendpoint/IHardwareAudioEngineBase::SetGfxState, coreaudio.ihardwareaudioenginebase_setgfxstate
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
 - IHardwareAudioEngineBase.SetGfxState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHardwareAudioEngineBase::SetGfxState


## -description


The <b>SetGfxState</b> method sets the GFX state of the offloaded audio stream.


## -parameters




### -param pDevice [in]

Pointer to an <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interface.


### -param _bEnable

TBD




#### - pbEnable [in]

Pointer to a boolean variable.


## -returns



The <b>SetGfxState</b> method returns S_OK to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24">IHardwareAudioEngineBase</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a>
 

 

