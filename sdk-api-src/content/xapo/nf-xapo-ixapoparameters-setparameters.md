---
UID: NF:xapo.IXAPOParameters.SetParameters
title: IXAPOParameters::SetParameters
author: windows-sdk-content
description: Sets effect-specific parameters.
old-location: xaudio2\ixapoparameters_interface_setparameters.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapoparameters.IXAPOParameters.SetParameters(const void,UINT32)
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IXAPOParameters interface [XAudio2 Audio Mixing APIs],SetParameters method, IXAPOParameters.SetParameters, IXAPOParameters::SetParameters, SetParameters, SetParameters method [XAudio2 Audio Mixing APIs], SetParameters method [XAudio2 Audio Mixing APIs],IXAPOParameters interface, xapo/IXAPOParameters::SetParameters, xaudio2.ixapoparameters_interface_setparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapo.h
req.include-header: 
req.redist: 
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
req.typenames: XAPO_BUFFER_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPO.h
api_name:
 - IXAPOParameters.SetParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPOParameters::SetParameters


## -description


Sets effect-specific parameters.


## -parameters




### -param pParameters

Effect-specific parameter block.


### -param ParameterByteSize

Size of pParameters, in bytes.


## -returns



This method does not return a value.




## -remarks



The data in <i>pParameters</i> is completely effect-specific and determined by the implementation of the <b>IXAPOParameters::SetParameters</b> function. The data passed to <b>SetParameters</b> can be used to set the state of the XAPO and control the behavior of the <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> function.



<b>SetParameters</b> can only be called on the real-time audio processing thread; no synchronization between <b>SetParameters</b> and the <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> method is necessary. However, the <a href="https://msdn.microsoft.com/7A5217AE-D7D6-4D92-A14E-DA36854F4D3E">IXAudio2Voice::SetEffectParameters</a> method may be called from any thread as it adds in the required synchronization to deliver a copy (asynchronously) of the parameters to <b>SetParameters</b> on the real-time thread; no synchronization between <b>IXAudio2Voice::SetEffectParameters</b> and the <b>IXAPO::Process</b> method is necessary.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/0CB2BA7E-5115-449C-A538-44EDCAFFE96F">IXAPOParameters</a>



<a href="https://msdn.microsoft.com/7A5217AE-D7D6-4D92-A14E-DA36854F4D3E">IXAudio2Voice::SetEffectParameters</a>
 

 

