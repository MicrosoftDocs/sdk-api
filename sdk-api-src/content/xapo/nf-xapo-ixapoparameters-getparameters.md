---
UID: NF:xapo.IXAPOParameters.GetParameters
title: IXAPOParameters::GetParameters
author: windows-sdk-content
description: Gets the current values for any effect-specific parameters.
old-location: xaudio2\ixapoparameters_interface_getparameters.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapoparameters.IXAPOParameters.GetParameters(void@,UINT32)
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetParameters, GetParameters method [XAudio2 Audio Mixing APIs], GetParameters method [XAudio2 Audio Mixing APIs],IXAPOParameters interface, IXAPOParameters interface [XAudio2 Audio Mixing APIs],GetParameters method, IXAPOParameters.GetParameters, IXAPOParameters::GetParameters, xapo/IXAPOParameters::GetParameters, xaudio2.ixapoparameters_interface_getparameters
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
 - IXAPOParameters.GetParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAPOParameters::GetParameters


## -description


Gets the current values for any effect-specific parameters.


## -parameters




### -param pParameters [in, out]

Receives an effect-specific parameter block.


### -param ParameterByteSize [in]

Size of pParameters, in bytes.


## -returns



This method does not return a value.




## -remarks



The data in <i>pParameters</i> is completely effect-specific and determined by the implementation of the <b>IXAPOParameters::GetParameters</b> function. The data returned in <i>pParameters</i> can be used to provide information about the current state of the XAPO.



Unlike SetParameters, XAudio2 does not call this method on the realtime audio processing thread. Thus, the XAPO must protect variables shared with <a href="https://msdn.microsoft.com/1E6FD9FB-9E99-422E-B2E1-3679FC3EEF32">IXAPOParameters::SetParameters</a> or <a href="https://msdn.microsoft.com/2510590D-578A-4A39-847A-34DFE620A7CC">IXAPO::Process</a> using appropriate synchronization. The <a href="https://msdn.microsoft.com/70F46E4E-E4FC-434F-AB35-B32C1365BB6D">CXAPOParametersBase</a> class is an implementation of <a href="https://msdn.microsoft.com/0CB2BA7E-5115-449C-A538-44EDCAFFE96F">IXAPOParameters</a> and its implementation of <b>GetParameters</b> efficiently handles this synchronization for the user.



XAudio2 calls this method from the <a href="https://msdn.microsoft.com/75CC5E5D-74B2-4972-9E1D-D6CB4A3034CD">IXAudio2Voice::GetEffectParameters</a> method.



This method may block and should never be called from the realtime audio processing thread instead get the current parameters from <a href="https://msdn.microsoft.com/BC386533-FD78-4CE5-8CE7-E156EE92D500">CXAPOParametersBase::BeginProcess</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/0CB2BA7E-5115-449C-A538-44EDCAFFE96F">IXAPOParameters</a>



<a href="https://msdn.microsoft.com/75CC5E5D-74B2-4972-9E1D-D6CB4A3034CD">IXAudio2Voice::GetEffectParameters</a>
 

 

