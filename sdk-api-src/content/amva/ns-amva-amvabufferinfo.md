---
UID: NS:amva._tag_AMVABUFFERINFO
title: AMVABUFFERINFO (amva.h)
description: The AMVABUFFERINFO structure specifies a buffer for the IAMVideoAccelerator::Execute method.
helpviewer_keywords: ["*LPAMVABUFFERINFO","AMVABUFFERINFO","AMVABUFFERINFO structure [DirectShow]","AMVABUFFERINFOStructure","DXVA_ALPHA_BLEND_COMBINATION_BUFFER","DXVA_AYUV_BUFFER","DXVA_BITSTREAM_DATA_BUFFER","DXVA_DCCMD_SURFACE_BUFFER","DXVA_DEBLOCKING_CONTROL_BUFFER","DXVA_DPXD_SURFACE_BUFFER","DXVA_HIGHLIGHT_BUFFER","DXVA_IA44_SURFACE_BUFFER","DXVA_INVERSE_QUANTIZATION_MATRIX_BUFFER","DXVA_MACROBLOCK_CONTROL_BUFFER","DXVA_PICTURE_DECODE_BUFFER","DXVA_PICTURE_RESAMPLE_BUFFER","DXVA_READ_BACK_BUFFER","DXVA_RESIDUAL_DIFFERENCE_BUFFER","DXVA_SLICE_CONTROL_BUFFER","LPAMVABUFFERINFO","LPAMVABUFFERINFO structure pointer [DirectShow]","amva/AMVABUFFERINFO","amva/LPAMVABUFFERINFO","dshow.amvabufferinfo"]
old-location: dshow\amvabufferinfo.htm
tech.root: dshow
ms.assetid: 8b018c40-44ae-4033-97b3-efa4b4c1bfb2
ms.date: 4/26/2023
ms.keywords: '*LPAMVABUFFERINFO, AMVABUFFERINFO, AMVABUFFERINFO structure [DirectShow], AMVABUFFERINFOStructure, DXVA_ALPHA_BLEND_COMBINATION_BUFFER, DXVA_AYUV_BUFFER, DXVA_BITSTREAM_DATA_BUFFER, DXVA_DCCMD_SURFACE_BUFFER, DXVA_DEBLOCKING_CONTROL_BUFFER, DXVA_DPXD_SURFACE_BUFFER, DXVA_HIGHLIGHT_BUFFER, DXVA_IA44_SURFACE_BUFFER, DXVA_INVERSE_QUANTIZATION_MATRIX_BUFFER, DXVA_MACROBLOCK_CONTROL_BUFFER, DXVA_PICTURE_DECODE_BUFFER, DXVA_PICTURE_RESAMPLE_BUFFER, DXVA_READ_BACK_BUFFER, DXVA_RESIDUAL_DIFFERENCE_BUFFER, DXVA_SLICE_CONTROL_BUFFER, LPAMVABUFFERINFO, LPAMVABUFFERINFO structure pointer [DirectShow], amva/AMVABUFFERINFO, amva/LPAMVABUFFERINFO, dshow.amvabufferinfo'
req.header: amva.h
req.include-header: Videoacc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: AMVABUFFERINFO, *LPAMVABUFFERINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tag_AMVABUFFERINFO
 - amva/_tag_AMVABUFFERINFO
 - LPAMVABUFFERINFO
 - amva/LPAMVABUFFERINFO
 - AMVABUFFERINFO
 - amva/AMVABUFFERINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amva.h
api_name:
 - AMVABUFFERINFO
---

# AMVABUFFERINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AMVABUFFERINFO</b> structure specifies a buffer for the 
        <a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute">IAMVideoAccelerator::Execute</a>  method.

## -struct-fields

### -field dwTypeIndex

Type of buffer. The following buffer types are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA_ALPHA_BLEND_COMBINATION_BUFFER"></a><a id="dxva_alpha_blend_combination_buffer"></a><dl>
<dt><b>DXVA_ALPHA_BLEND_COMBINATION_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Alpha blend combination buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_AYUV_BUFFER"></a><a id="dxva_ayuv_buffer"></a><dl>
<dt><b>DXVA_AYUV_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
AYUV alpha blending sample buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_BITSTREAM_DATA_BUFFER"></a><a id="dxva_bitstream_data_buffer"></a><dl>
<dt><b>DXVA_BITSTREAM_DATA_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Raw bitstream data buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_DCCMD_SURFACE_BUFFER"></a><a id="dxva_dccmd_surface_buffer"></a><dl>
<dt><b>DXVA_DCCMD_SURFACE_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Display control command (DCCMD) data buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_DEBLOCKING_CONTROL_BUFFER"></a><a id="dxva_deblocking_control_buffer"></a><dl>
<dt><b>DXVA_DEBLOCKING_CONTROL_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Deblocking Filter control command buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_DPXD_SURFACE_BUFFER"></a><a id="dxva_dpxd_surface_buffer"></a><dl>
<dt><b>DXVA_DPXD_SURFACE_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Decoded PXD (DPXD) alpha blending surface buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_HIGHLIGHT_BUFFER"></a><a id="dxva_highlight_buffer"></a><dl>
<dt><b>DXVA_HIGHLIGHT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Highlight data buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_IA44_SURFACE_BUFFER"></a><a id="dxva_ia44_surface_buffer"></a><dl>
<dt><b>DXVA_IA44_SURFACE_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
IA44 alpha blending sample buffer. 

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_INVERSE_QUANTIZATION_MATRIX_BUFFER"></a><a id="dxva_inverse_quantization_matrix_buffer"></a><dl>
<dt><b>DXVA_INVERSE_QUANTIZATION_MATRIX_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Inverse quantization matrix buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_MACROBLOCK_CONTROL_BUFFER"></a><a id="dxva_macroblock_control_buffer"></a><dl>
<dt><b>DXVA_MACROBLOCK_CONTROL_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Macroblock control command buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_PICTURE_DECODE_BUFFER"></a><a id="dxva_picture_decode_buffer"></a><dl>
<dt><b>DXVA_PICTURE_DECODE_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Picture parameters buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_PICTURE_RESAMPLE_BUFFER"></a><a id="dxva_picture_resample_buffer"></a><dl>
<dt><b>DXVA_PICTURE_RESAMPLE_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Alpha blend combination buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_READ_BACK_BUFFER"></a><a id="dxva_read_back_buffer"></a><dl>
<dt><b>DXVA_READ_BACK_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Read-back command buffers containing commands to read macroblocks of the resulting picture back to the host.

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_RESIDUAL_DIFFERENCE_BUFFER"></a><a id="dxva_residual_difference_buffer"></a><dl>
<dt><b>DXVA_RESIDUAL_DIFFERENCE_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Residual difference block data buffer. 

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA_SLICE_CONTROL_BUFFER"></a><a id="dxva_slice_control_buffer"></a><dl>
<dt><b>DXVA_SLICE_CONTROL_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Slice control buffer.

</td>
</tr>
</table>
 

For complete descriptions of these buffer types, refer to the DirectX Video Acceleration 1.0 specification.

### -field dwBufferIndex

Buffer index.

### -field dwDataOffset

The offset of the relevant data from the beginning of the buffer.

### -field dwDataSize

Size of the relevant data in the buffer, in bytes.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute">IAMVideoAccelerator::Execute</a>