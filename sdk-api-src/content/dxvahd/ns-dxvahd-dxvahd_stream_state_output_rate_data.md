---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
title: DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
author: windows-sdk-content
description: Specifies the output frame rate for an input stream when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_stream_state_output_rate_data.htm
tech.root: medfound
ms.assetid: 9cca24f0-5fff-4125-b1fe-d2f9278b5181
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA, DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA structure [Media Foundation], FALSE, TRUE, dxvahd/DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA, mf.dxvahd_stream_state_output_rate_data
ms.topic: struct
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA
req.redist: 
---

# DXVAHD_STREAM_STATE_OUTPUT_RATE_DATA structure


## -description


Specifies the output frame rate for an input stream when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field RepeatFrame

Specifies how the device performs frame-rate conversion, if required. The default state value is <b>FALSE</b> (interpolation).

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
The device repeats frames.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The device interpolates frames.

</td>
</tr>
</table>
 


### -field OutputRate

Specifies the output rate, as a member of the <a href="https://msdn.microsoft.com/f96184d8-c5c2-4767-899f-323935fa9e89">DXVAHD_OUTPUT_RATE</a> enumeration.


### -field CustomRate

Specifies a custom output rate, as a <a href="https://msdn.microsoft.com/8064820e-533e-4b40-8eeb-e3ad6a6b1ff7">DXVAHD_RATIONAL</a> structure. This member is ignored unless <b>OutputRate</b> equals <b>DXVAHD_OUTPUT_RATE_CUSTOM</b>. The default state value is 1/1.

To get the list of custom rates supported by the video processor, call <a href="https://msdn.microsoft.com/63e835bb-dda2-4449-8474-219a373da82d">IDXVAHD_Device::GetVideoProcessorCustomRates</a>. If a custom rate is used, it must be taken from this list.


## -remarks



The output rate might require the device to convert the frame rate of the input stream. If so, the value of <b>RepeatFrame</b> controls whether the device creates interpolated frames or simply repeats input frames.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

