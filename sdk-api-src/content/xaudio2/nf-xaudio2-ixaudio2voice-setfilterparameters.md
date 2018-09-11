---
UID: NF:xaudio2.IXAudio2Voice.SetFilterParameters
title: IXAudio2Voice::SetFilterParameters
author: windows-sdk-content
description: Sets the voice's filter parameters.
old-location: xaudio2\ixaudio2voice_interface_setfilterparameters.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.SetFilterParameters(const XAUDIO2_FILTER_PARAMETERS,UINT32)
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IXAudio2Voice interface [XAudio2 Audio Mixing APIs],SetFilterParameters method, IXAudio2Voice.SetFilterParameters, IXAudio2Voice::SetFilterParameters, SetFilterParameters, SetFilterParameters method [XAudio2 Audio Mixing APIs], SetFilterParameters method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, xaudio2.ixaudio2voice_interface_setfilterparameters, xaudio2/IXAudio2Voice::SetFilterParameters
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
 - IXAudio2Voice.SetFilterParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2Voice::SetFilterParameters


## -description


Sets the voice's filter parameters.


## -parameters




### -param pParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/ac0971d3-92cc-41c1-836a-77df89baa750">XAUDIO2_FILTER_PARAMETERS</a> structure containing the filter information. 


### -param X2DEFAULT

TBD




#### - OperationSet [in]

Identifies this call as part of a deferred batch. See the <a href="https://msdn.microsoft.com/5bfd747d-af65-f619-e549-be8130748261">XAudio2 Operation Sets</a> overview for more information.


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of error codes. 




## -remarks



<b>SetFilterParameters</b> will fail if the voice was not created with the XAUDIO2_VOICE_USEFILTER flag.



This method is usable only on source and submix voices and has no effect on mastering voices.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/7E5B3896-A415-4E06-94EB-F9205B3CFB32">IXAudio2Voice::GetFilterParameters</a> always returns this voice's actual current filter parameters. However, these may not match the parameters set by the most recent <b>IXAudio2Voice::SetFilterParameters</b> call: the actual parameters are only changed the next time the audio engine runs after the <b>IXAudio2Voice::SetFilterParameters</b> call (or after the corresponding <a href="https://msdn.microsoft.com/2E798B7B-AD3E-4DCD-BB88-BAD3EC64EFE1">IXAudio2::CommitChanges</a> call, if <b>IXAudio2Voice::SetFilterParameters</b> was called with a deferred operation ID).</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>
 

 

