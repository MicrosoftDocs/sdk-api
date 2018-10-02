---
UID: NF:xaudio2.IXAudio2Voice.GetOutputFilterParameters
title: IXAudio2Voice::GetOutputFilterParameters
author: windows-sdk-content
description: Returns the filter parameters from one of this voice's sends.
old-location: xaudio2\ixaudio2voice_interface_getoutputfilterparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.GetOutputFilterParameters(IXAudio2Voice,XAUDIO2_FILTER_PARAMETERS@)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetOutputFilterParameters, GetOutputFilterParameters method [XAudio2 Audio Mixing APIs], GetOutputFilterParameters method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],GetOutputFilterParameters method, IXAudio2Voice.GetOutputFilterParameters, IXAudio2Voice::GetOutputFilterParameters, xaudio2.ixaudio2voice_interface_getoutputfilterparameters, xaudio2/IXAudio2Voice::GetOutputFilterParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xaudio2.h
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
 - xaudio2.h
api_name:
 - IXAudio2Voice.GetOutputFilterParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2Voice::GetOutputFilterParameters


## -description


Returns the filter parameters from one of this voice's sends.


## -parameters




### -param pDestinationVoice [in]


<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a> pointer to the destination voice of the send whose filter parameters will be read.


### -param pParameters [out]

Pointer to an <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> structure containing the filter information.


## -returns



This method does not return a value.




## -remarks



<b>GetOutputFilterParameters</b> will fail if the send was not created with the XAUDIO2_SEND_USEFILTER flag. This method is usable only on sends belonging to source and submix voices and has no effect on mastering voices’ sends.



<div class="alert"><b>Note</b>  <b>IXAudio2Voice::GetOutputFilterParameters</b> always returns this send’s actual current filter parameters. However, these may not match the parameters set by the most recent <a href="https://msdn.microsoft.com/A707A64A-D929-4387-AABC-30E7AAECB99B">IXAudio2Voice::SetOutputFilterParameters</a> call: the actual parameters are only changed the next time the audio engine runs after the <b>IXAudio2Voice::SetOutputFilterParameters</b> call (or after the corresponding <a href="https://msdn.microsoft.com/2E798B7B-AD3E-4DCD-BB88-BAD3EC64EFE1">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetOutputFilterParameters</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>
 

 

