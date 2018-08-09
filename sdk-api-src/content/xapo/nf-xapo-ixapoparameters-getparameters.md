---
UID: NF:xapo.IXAPOParameters.GetParameters
title: IXAPOParameters::GetParameters
author: windows-sdk-content
description: Gets the current values for any effect-specific parameters.
old-location: xaudio2\ixapoparameters_interface_getparameters.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixapoparameters.IXAPOParameters.GetParameters(void@,UINT32)
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetParameters, GetParameters method [XAudio2 Audio Mixing APIs], GetParameters method [XAudio2 Audio Mixing APIs],IXAPOParameters interface, IXAPOParameters interface [XAudio2 Audio Mixing APIs],GetParameters method, IXAPOParameters.GetParameters, IXAPOParameters::GetParameters, xapo/IXAPOParameters::GetParameters, xaudio2.ixapoparameters_interface_getparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xapo.h
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



Unlike SetParameters, XAudio2 does not call this method on the realtime audio processing thread. Thus, the XAPO must protect variables shared with <a href="https://msdn.microsoft.com/en-us/library/Ee418447(v=VS.85).aspx">IXAPOParameters::SetParameters</a> or <a href="https://msdn.microsoft.com/en-us/library/Ee418456(v=VS.85).aspx">IXAPO::Process</a> using appropriate synchronization. The <a href="https://msdn.microsoft.com/en-us/library/Ee415238(v=VS.85).aspx">CXAPOParametersBase</a> class is an implementation of <a href="https://msdn.microsoft.com/en-us/library/Ee415896(v=VS.85).aspx">IXAPOParameters</a> and its implementation of <b>GetParameters</b> efficiently handles this synchronization for the user.



XAudio2 calls this method from the <a href="https://msdn.microsoft.com/en-us/library/Ee418586(v=VS.85).aspx">IXAudio2Voice::GetEffectParameters</a> method.



This method may block and should never be called from the realtime audio processing thread instead get the current parameters from <a href="https://msdn.microsoft.com/en-us/library/Ee416384(v=VS.85).aspx">CXAPOParametersBase::BeginProcess</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415896(v=VS.85).aspx">IXAPOParameters</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee418586(v=VS.85).aspx">IXAudio2Voice::GetEffectParameters</a>
 

 

