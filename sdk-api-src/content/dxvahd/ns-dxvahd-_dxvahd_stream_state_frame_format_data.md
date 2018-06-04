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

# _DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA structure


## -description


Specifies how a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream is interlaced.


## -struct-fields




### -field FrameFormat

The video interlacing, specified as a <a href="https://msdn.microsoft.com/fc720dd3-e9c1-4b92-ac09-8e53cff44bec">DXVAHD_FRAME_FORMAT</a> value.

The default state value is <b>DXVAHD_FRAME_FORMAT_PROGRESSIVE</b> (progressive frames).


## -remarks



Some devices do not support interlaced RGB. Interlaced RGB support is indicated by the <b>DXVAHD_INPUT_FORMAT_CAPS_RGB_INTERLACED</b>  capability flag. If the device does not support interlaced RGB, it treats all RGB input streams as progressive frames. 

Some devices do not support interlaced formats with palettized color. This support is indicated by the <b>DXVAHD_INPUT_FORMAT_CAPS_PALETTE_INTERLACED</b> flag. If the device does not support this capability, all palettized input streams are treated as progressive frames.

To get the device's capabilities, call <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>InputFormatCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DXVAHD_SetFrameFormat(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    DXVAHD_FRAME_FORMAT format
    )
{
    DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { format };

    HRESULT hr = pVP-&gt;SetVideoProcessStreamState(
        stream,
        DXVAHD_STREAM_STATE_FRAME_FORMAT,
        sizeof(frame_format),
        &amp;frame_format
        );

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

