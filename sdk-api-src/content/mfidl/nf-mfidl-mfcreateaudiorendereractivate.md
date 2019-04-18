---
UID: NF:mfidl.MFCreateAudioRendererActivate
title: MFCreateAudioRendererActivate function (mfidl.h)
author: windows-sdk-content
description: Creates an activation object for the Streaming Audio Renderer.
old-location: mf\mfcreateaudiorendereractivate.htm
tech.root: medfound
ms.assetid: bce55c34-d64a-4f3b-8d09-6c9363e4eb11
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFCreateAudioRendererActivate, MFCreateAudioRendererActivate function [Media Foundation], bce55c34-d64a-4f3b-8d09-6c9363e4eb11, mf.mfcreateaudiorendereractivate, mfidl/MFCreateAudioRendererActivate
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateAudioRendererActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateAudioRendererActivate function


## -description



Creates an activation object for the <a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>.




## -parameters




### -param ppActivate [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. Use this interface to create the audio renderer. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create the audio renderer, call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> on the retrieved <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointer.

<div class="alert"><b>Note</b>  To avoid a memory leak, call <a href="https://msdn.microsoft.com/1f88ff31-5a91-4838-bfce-673a5a85c766">IMFActivate::ShutdownObject</a> before releasing the final reference to the audio renderer or the audio renderer activate object.</div>
<div> </div>
To configure the audio renderer, set any of the following attributes on the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> object before calling <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a>. (If you are using the Media Session, the Media Session automatically calls <b>ActivateObject</b> when you queue the topology.)

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f145fb80-c136-421c-9a65-e69c52109348">MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID</a>
</td>
<td>The audio endpoint device identifier.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f0456337-5351-457e-9830-920bf346bfc4">MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE</a>
</td>
<td>The audio endpoint role.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/07433904-1bf6-4e8d-9571-8d663bf4fd13">MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS</a>
</td>
<td>Miscellaneous configuration flags.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/80b028f5-7756-4bb8-b5e3-ebc8343e168c">MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID</a>
</td>
<td>The audio policy class.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/88E79DE6-2062-4471-A939-D1D4DD2EC42D">MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY</a>
</td>
<td>The audio stream category.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4D11B4D6-8CFF-4850-BF8F-9019A1F79153">MF_LOW_LATENCY</a>
</td>
<td>Enables low-latency audio streaming.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

