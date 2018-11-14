---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_ALPHA_DATA
title: "_DXVAHD_STREAM_STATE_ALPHA_DATA"
author: windows-sdk-content
description: Specifies the planar alpha value for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_stream_state_alpha_data.htm
tech.root: medfound
ms.assetid: 51135d6e-4f97-44d9-b1d5-f7d2095ee6f1
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DXVAHD_STREAM_STATE_ALPHA_DATA, DXVAHD_STREAM_STATE_ALPHA_DATA structure [Media Foundation], _DXVAHD_STREAM_STATE_ALPHA_DATA, dxvahd/DXVAHD_STREAM_STATE_ALPHA_DATA, mf.dxvahd_stream_state_alpha_data
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DXVAHD_STREAM_STATE_ALPHA_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_ALPHA_DATA
req.redist: 
---

# _DXVAHD_STREAM_STATE_ALPHA_DATA structure


## -description


Specifies the planar alpha value for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field Enable

<b>If TRUE</b>, alpha blending is enabled. Otherwise, alpha blending is disabled. The default state value is <b>FALSE</b>.


### -field Alpha

Specifies the planar alpha value as a floating-point number from 0.0 (transparent) to 1.0 (opaque). 

If the <b>Enable</b> member is <b>FALSE</b>, this member is ignored.


## -remarks



For each pixel, the destination color value is computed as follows:

<code>Cd = Cs * (As * Ap * Ae) + Cd * (1.0 - As * Ap * Ae)</code>

where

<ul>
<li><code>Cd</code> = Color value of the destination pixel.</li>
<li><code>Cs</code> = Color value of source pixel.</li>
<li><code>As</code> = Per-pixel source alpha.</li>
<li><code>Ap</code> = Planar alpha value.</li>
<li><code>Ae</code> = Palette-entry alpha value, or 1.0 (see Note).</li>
</ul>
<div class="alert"><b>Note</b>  Palette-entry alpha values apply only to palettized color formats, and only when the device supports the <b>DXVAHD_FEATURE_CAPS_ALPHA_PALETTE</b> capability. Otherwise, this factor equals 1.0. </div>
<div> </div>
The destination alpha value is computed according to the <b>DXVAHD_BLT_STATE_ALPHA_FILL</b> state. For more information, see <a href="https://msdn.microsoft.com/dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>.

To get the device capabilities, call <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> and check the <b>FeatureCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DXVAHD_SetPlanarAlpha(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    BOOL bEnable,
    float fAlpha
    )
{
    DXVAHD_STREAM_STATE_ALPHA_DATA alpha = { bEnable, fAlpha };

    HRESULT hr = pVP-&gt;SetVideoProcessStreamState(
        stream,
        DXVAHD_STREAM_STATE_ALPHA,
        sizeof(alpha),
        &amp;alpha
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
 

 

