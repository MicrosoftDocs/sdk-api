---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_LUMA_KEY_DATA
title: DXVAHD_STREAM_STATE_LUMA_KEY_DATA
author: windows-sdk-content
description: Specifies the luma key for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_stream_state_luma_key_data.htm
tech.root: medfound
ms.assetid: d94b04d9-9d94-4392-a0bf-a33210aeef1f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXVAHD_STREAM_STATE_LUMA_KEY_DATA, DXVAHD_STREAM_STATE_LUMA_KEY_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_LUMA_KEY_DATA, mf.dxvahd_stream_state_luma_key_data
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
 - DXVAHD_STREAM_STATE_LUMA_KEY_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_LUMA_KEY_DATA
req.redist: 
---

# DXVAHD_STREAM_STATE_LUMA_KEY_DATA structure


## -description


Specifies the luma key for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field Enable

If <b>TRUE</b>, luma keying is enabled. Otherwise, luma keying is disabled. The default value is <b>FALSE</b>.




### -field Lower

The lower bound for the luma key. The range is [0…1]. The default state value is 0.0. 


### -field Upper

The upper bound for the luma key. The range is [0…1]. The default state value is 0.0. 


## -remarks



To use this state, the device must support luma keying, indicated by the <b>DXVAHD_FEATURE_CAPS_LUMA_KEY</b> capability flag. To query for this capability, call <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a>. If the device supports luma keying, it sets the  <b>DXVAHD_FEATURE_CAPS_LUMA_KEY</b> flag in the <b>FeatureCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure.

If the device does not support luma keying, the <a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a> method fails for this state.

If the input format is RGB, the device must also support the <b>DXVAHD_INPUT_FORMAT_CAPS_RGB_LUMA_KEY</b> capability. This capability flag is set in the <b>InputFormatCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure. If the flag is not present, the device ignores the luma key value for RGB input.

The values of <b>Lower</b> and <b>Upper</b> give the lower and upper bounds of the luma key, using a nominal range of [0...1]. Given a format with <i>n</i> bits per channel, these values are converted to luma values as follows:

<code>val = f * ((1 &lt;&lt; n)-1)</code>

Any pixel whose luma value falls within the upper and lower bounds (inclusive) is treated as transparent.

For example, if the pixel format uses 8-bit luma, the upper bound is calculated as follows:

<code>BYTE Y = BYTE(max(min(1.0, Upper), 0.0) * 255.0)</code>

Note that the value is clamped to the range [0...1] before multiplying by 255.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DXVAHD_SetLumaKey(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    BOOL bEnable,
    float fLower,   // Lower bound for the luma key.
    float fUpper    // Uppper bound for the luma key.
    )
{
    DXVAHD_STREAM_STATE_LUMA_KEY_DATA luma = { bEnable, fLower, fUpper };

    HRESULT hr = pVP-&gt;SetVideoProcessStreamState(
        stream,
        DXVAHD_STREAM_STATE_LUMA_KEY,
        sizeof(luma),
        &amp;luma
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
 

 

