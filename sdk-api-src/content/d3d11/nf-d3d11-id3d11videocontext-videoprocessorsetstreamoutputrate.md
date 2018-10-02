---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamOutputRate
title: ID3D11VideoContext::VideoProcessorSetStreamOutputRate
author: windows-sdk-content
description: Sets the rate at which the video processor produces output frames for an input stream.
old-location: mf\id3d11videocontext_videoprocessorsetstreamoutputrate.htm
tech.root: MedFound
ms.assetid: D353F6E8-B465-46CB-AA47-8B097AB4AF2A
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FALSE, ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamOutputRate method, ID3D11VideoContext.VideoProcessorSetStreamOutputRate, ID3D11VideoContext::VideoProcessorSetStreamOutputRate, TRUE, VideoProcessorSetStreamOutputRate, VideoProcessorSetStreamOutputRate method [Media Foundation], VideoProcessorSetStreamOutputRate method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamOutputRate, mf.id3d11videocontext_videoprocessorsetstreamoutputrate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorSetStreamOutputRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamOutputRate


## -description


Sets the rate at which the video processor produces output frames for an input stream.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param OutputRate [in]

The output rate, specified as a <a href="https://msdn.microsoft.com/C950E5B5-E50C-4750-83F3-38296EF2009F">D3D11_VIDEO_PROCESSOR_OUTPUT_RATE</a> value.


### -param RepeatFrame [in]

Specifies how the driver performs frame-rate conversion, if required.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Repeat frames.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Interpolate frames.

</td>
</tr>
</table>
 


### -param pCustomRate [in]

A pointer to a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure. If <i>OutputRate</i> is <b>D3D11_VIDEO_PROCESSOR_OUTPUT_RATE_CUSTOM</b>,  this parameter specifies the exact output rate. Otherwise, this parameter is ignored and can be <b>NULL</b>.


## -returns



This method does not return a value.




## -remarks



The standard output rates are normal frame-rate (<b>D3D11_VIDEO_PROCESSOR_OUTPUT_RATE_NORMAL</b>) and half frame-rate (<b>D3D11_VIDEO_PROCESSOR_OUTPUT_RATE_HALF</b>). In addition, the driver might support custom rates  for rate conversion or inverse telecine. To get the list of custom rates, call <a href="https://msdn.microsoft.com/0FA868E6-B0FB-433B-A183-72DDE39B207E">ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate</a>.

Depending on the output rate, the driver might need to convert the frame rate. If so, the value of <i>RepeatFrame</i> controls whether the driver creates interpolated frames or simply repeats input frames.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

