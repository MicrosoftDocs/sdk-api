---
UID: NF:audioengineendpoint.IHardwareAudioEngineBase.GetGfxState
title: IHardwareAudioEngineBase::GetGfxState method
author: windows-driver-content
description: The GetGfxState method retrieves the GFX state of the offloaded audio stream.
old-location: coreaudio\ihardwareaudioenginebase_getgfxstate.htm
old-project: CoreAudio
ms.assetid: 519D3BF1-B5C3-469A-A188-7D741E288337
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetGfxState method [Core Audio], GetGfxState method [Core Audio], IHardwareAudioEngineBase interface, GetGfxState,IHardwareAudioEngineBase.GetGfxState, IHardwareAudioEngineBase, IHardwareAudioEngineBase interface [Core Audio], GetGfxState method, IHardwareAudioEngineBase::GetGfxState, audioengineendpoint/IHardwareAudioEngineBase::GetGfxState, coreaudio.ihardwareaudioenginebase_getgfxstate
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
req.typenames: AE_POSITION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	audioengineendpoint.h
api_name:
-	IHardwareAudioEngineBase.GetGfxState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IHardwareAudioEngineBase::GetGfxState method


## -description


The <b>GetGfxState</b> method retrieves the GFX state of the offloaded audio stream.


## -parameters




### -param pDevice [in]

Pointer to an <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interface.


### -param _pbEnable [out]

Pointer to a boolean variable.


## -returns



The <b>GetGfxState</b> method returns S_OK to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24">IHardwareAudioEngineBase</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a>
 

 

