---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ReverbConvertI3DL2ToNative function


## -description


Inline function that converts I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) parameters to native XAudio2 parameters.


## -parameters




### -param pI3DL2 [in]

Pointer to a <a href="https://msdn.microsoft.com/17ec91d0-ee68-4b44-875f-1dcaec0f5381">XAUDIO2FX_REVERB_I3DL2_PARAMETERS</a> structure containing the I3DL2 parameters to convert. There are many preset values defined for the <b>XAUDIO2FX_REVERB_I3DL2_PARAMETERS</b> structure; for more information, see <a href="https://msdn.microsoft.com/6dcf4fe8-1189-8b79-b94b-29af835e4bcd">XAUDIO2FX_I3DL2_PRESET</a>.


### -param pNative [in, out]

Pointer to a <a href="https://msdn.microsoft.com/ddcb16ce-5d77-4417-a267-b33208065e5c">XAUDIO2FX_REVERB_PARAMETERS</a> structure that will receive the native parameters that are equivalent to the I3DL2 parameters. 


### -param sevenDotOneReverb

A boolean value indicating whether 7.1 reverb is enabled.

<div class="alert"><b>Note</b>  This parameter is supported beginning with Windows 10.</div>
<div> </div>

## -returns



This function does not return a value.




## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/6dcf4fe8-1189-8b79-b94b-29af835e4bcd">XAUDIO2FX_I3DL2_PRESET</a>



<a href="https://msdn.microsoft.com/17ec91d0-ee68-4b44-875f-1dcaec0f5381">XAUDIO2FX_REVERB_I3DL2_PARAMETERS</a>



<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">XAudio2::Functions</a>
 

 

