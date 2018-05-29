---
UID: NF:mfidl.MFCreateAudioRenderer
title: MFCreateAudioRenderer function
author: windows-sdk-content
description: Creates the Streaming Audio Renderer.
old-location: mf\mfcreateaudiorenderer.htm
old-project: medfound
ms.assetid: 9554e39b-9d14-4b7f-862c-a1ffcf84543c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 9554e39b-9d14-4b7f-862c-a1ffcf84543c, MFCreateAudioRenderer, MFCreateAudioRenderer function [Media Foundation], mf.mfcreateaudiorenderer, mfidl/MFCreateAudioRenderer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateAudioRenderer
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateAudioRenderer function


## -description



          Creates the <a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>.
        


## -parameters




### -param pAudioAttributes [in]


            A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface, which is used to configure the audio renderer. This parameter can be <b>NULL</b>. See Remarks.
          


### -param ppSink [out]


            Receives a pointer to the audio renderer's <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To configure the audio renderer, set any of the following attributes on the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface specified in the <i>pAudioAttributes</i> parameter.

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




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

