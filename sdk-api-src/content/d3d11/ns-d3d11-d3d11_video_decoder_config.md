---
UID: NS:d3d11.D3D11_VIDEO_DECODER_CONFIG
title: D3D11_VIDEO_DECODER_CONFIG (d3d11.h)
description: Describes the configuration of a Microsoft Direct3D 11 decoder device for DirectX Video Acceleration (DXVA).
helpviewer_keywords: ["D3D11_VIDEO_DECODER_CONFIG","D3D11_VIDEO_DECODER_CONFIG structure [Media Foundation]","d3d11/D3D11_VIDEO_DECODER_CONFIG","mf.d3d11_video_decoder_config"]
old-location: mf\d3d11_video_decoder_config.htm
tech.root: mf
ms.assetid: AB963FAD-F16C-47F6-8C78-FF4C234FBC60
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_DECODER_CONFIG, D3D11_VIDEO_DECODER_CONFIG structure [Media Foundation], d3d11/D3D11_VIDEO_DECODER_CONFIG, mf.d3d11_video_decoder_config
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
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_CONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_DECODER_CONFIG
 - d3d11/D3D11_VIDEO_DECODER_CONFIG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_CONFIG
---

# D3D11_VIDEO_DECODER_CONFIG structure


## -description

Describes the configuration of a Microsoft Direct3D 11 decoder device for DirectX Video Acceleration (DXVA).

## -struct-fields

### -field guidConfigBitstreamEncryption

If the bitstream data buffers are encrypted using the D3D11CryptoSession mechanism, this GUID should be set to zero. If no encryption is applied, the value is <b>DXVA_NoEncrypt</b>. If <b>ConfigBitstreamRaw</b> is 0, the value must be <b>DXVA_NoEncrypt</b>.

### -field guidConfigMBcontrolEncryption

If the macroblock control data buffers are  encrypted using the D3D11CryptoSession mechanism, this GUID should be set to zero.  If no encryption is applied, the value is <b>DXVA_NoEncrypt</b>. If <b>ConfigBitstreamRaw</b> is 1, the value must be <b>DXVA_NoEncrypt</b>.

### -field guidConfigResidDiffEncryption

If the residual difference decoding data buffers are  encrypted using the D3D11CryptoSession mechanism, this GUID should be set to zero.   If no encryption is applied, the value is <b>DXVA_NoEncrypt</b>. If <b>ConfigBitstreamRaw</b> is 1, the value must be <b>DXVA_NoEncrypt</b>.

### -field ConfigBitstreamRaw

Indicates whether the host-decoder sends raw bit-stream data. If the value is 1, the data for the pictures will be sent in bit-stream buffers as raw bit-stream content. If the value is 0, picture data will be sent using macroblock control command buffers. If either <b>ConfigResidDiffHost</b> or <b>ConfigResidDiffAccelerator</b> is 1, the value must be 0.

### -field ConfigMBcontrolRasterOrder

Specifies whether macroblock control commands are in raster scan order or in arbitrary order. If the value is 1, the macroblock control commands within each macroblock control command buffer are in raster-scan order. If the value is 0, the order is arbitrary. For some types of bit streams, forcing raster order either greatly increases the number of required macroblock control buffers that must be processed, or requires host reordering of the control information. Therefore, supporting arbitrary order can be more efficient.

### -field ConfigResidDiffHost

Contains the host residual difference configuration. If the value is 1, some residual difference decoding data may be sent as blocks in the spatial domain from the host. If the value is 0, spatial domain data will not be sent.

### -field ConfigSpatialResid8

Indicates the word size used to represent residual difference spatial-domain blocks for predicted (non-intra) pictures when using host-based residual difference decoding.
          

If <b>ConfigResidDiffHost</b> is 1 and <b>ConfigSpatialResid8</b> is 1, the host will send residual difference spatial-domain blocks for non-intra macroblocks using 8-bit signed samples and for intra macroblocks in predicted (non-intra) pictures in a format that depends on the value of <b>ConfigIntraResidUnsigned</b>:
          

<ul>
<li>If <b>ConfigIntraResidUnsigned</b> is 0, spatial-domain blocks for intra macroblocks are sent as 8-bit signed integer values relative to a constant reference value of 2^(BPP–1).
              </li>
<li>If <b>ConfigIntraResidUnsigned</b> is 1, spatial-domain blocks for intra macroblocks are sent as 8-bit unsigned integer values relative to a constant reference value of 0.
              </li>
</ul>
If <b>ConfigResidDiffHost</b> is 1 and <b>ConfigSpatialResid8</b> is 0, the host will send residual difference spatial-domain blocks of data for non-intra macroblocks using 16-bit signed samples and for intra macroblocks in predicted (non-intra) pictures in a format that depends on the value of <b>ConfigIntraResidUnsigned</b>:
          

<ul>
<li>If <b>ConfigIntraResidUnsigned</b> is 0, spatial domain blocks for intra macroblocks are sent as 16-bit signed integer values relative to a constant reference value of 2^(BPP–1).
              </li>
<li>If <b>ConfigIntraResidUnsigned</b> is 1, spatial domain blocks for intra macroblocks are sent as 16-bit unsigned integer values relative to a constant reference value of 0.
              </li>
</ul>
If <b>ConfigResidDiffHost</b> is 0, <b>ConfigSpatialResid8</b> must be 0.
          

For intra pictures, spatial-domain blocks must be sent using 8-bit samples if bits-per-pixel (BPP) is 8, and using 16-bit samples if BPP &gt; 8. If <b>ConfigIntraResidUnsigned</b> is 0, these samples are sent as signed integer values relative to a constant reference value of 2^(BPP–1), and if <b>ConfigIntraResidUnsigned</b> is 1, these samples are sent as unsigned integer values relative to a constant reference value of 0.

### -field ConfigResid8Subtraction

If the value is 1, 8-bit difference overflow blocks are subtracted rather than added. The value must be 0 unless <b>ConfigSpatialResid8</b> is 1.
          

The ability to subtract differences rather than add them enables 8-bit difference decoding to be fully compliant with the full ±255 range of values required in video decoder specifications, because +255 cannot be represented as the addition of two signed 8-bit numbers, but any number in the range ±255 can be represented as the difference between two signed 8-bit numbers (+255 = +127 minus –128).

### -field ConfigSpatialHost8or9Clipping

If the value is 1, spatial-domain blocks for intra macroblocks must be clipped to an 8-bit range on the host and spatial-domain blocks for non-intra macroblocks must be clipped to a 9-bit range on the host. If the value is 0, no such clipping is necessary by the host.
          

The value must be 0 unless <b>ConfigSpatialResid8</b> is 0 and <b>ConfigResidDiffHost</b> is 1.

### -field ConfigSpatialResidInterleaved

If the value is 1, any spatial-domain residual difference data must be sent in a chrominance-interleaved form matching the YUV format chrominance interleaving pattern. The value must be 0 unless <b>ConfigResidDiffHost</b> is 1 and the YUV format is NV12 or NV21.

### -field ConfigIntraResidUnsigned

Indicates the method of representation of spatial-domain blocks of residual difference data for intra blocks when using host-based difference decoding.
          

If <b>ConfigResidDiffHost</b> is 1 and <b>ConfigIntraResidUnsigned</b> is 0, spatial-domain residual difference data blocks for intra macroblocks must be sent as follows:
          

<ul>
<li>In a non-intra picture, if <b>ConfigSpatialResid8</b> is 0, the spatial-domain residual difference data blocks for intra macroblocks are sent as 16-bit signed integer values relative to a constant reference value of 2^(BPP–1).
              </li>
<li>In a non-intra picture, if <b>ConfigSpatialResid8</b> is 1, the spatial-domain residual difference data blocks for intra macroblocks are sent as 8-bit signed integer values relative to a constant reference value of 2^(BPP–1).
              </li>
<li>In an intra picture, if BPP is 8, the spatial-domain residual difference data blocks for intra macroblocks are sent as 8-bit signed integer values relative to a constant reference value of 2^(BPP–1), regardless of the value of <b>ConfigSpatialResid8</b>.
              </li>
</ul>
If <b>ConfigResidDiffHost</b> is 1 and <b>ConfigIntraResidUnsigned</b> is 1, spatial-domain residual difference data blocks for intra macroblocks must be sent as follows:
          

<ul>
<li>In a non-intra picture, if <b>ConfigSpatialResid8</b> is 0, the spatial-domain residual difference data blocks for intra macroblocks must be sent as 16-bit unsigned integer values relative to a constant reference value of 0.
              </li>
<li>In a non-intra picture, if <b>ConfigSpatialResid8</b> is 1, the spatial-domain residual difference data blocks for intra macroblocks are sent as 8-bit unsigned integer values relative to a constant reference value of 0.
              </li>
<li>In an intra picture, if BPP is 8, the spatial-domain residual difference data blocks for intra macroblocks are sent as 8-bit unsigned integer values relative to a constant reference value of 0, regardless of the value of <b>ConfigSpatialResid8</b>.
              </li>
</ul>
The value of the member must be 0 unless <b>ConfigResidDiffHost</b> is 1.

### -field ConfigResidDiffAccelerator

If the value is 1, transform-domain blocks of coefficient data may be sent from the host for accelerator-based IDCT. If the value is 0, accelerator-based IDCT will not be used. If both <b>ConfigResidDiffHost</b> and <b>ConfigResidDiffAccelerator</b> are 1, this indicates that some residual difference decoding will be done on the host and some on the accelerator, as indicated by macroblock-level control commands.
          

The value must be 0 if <b>ConfigBitstreamRaw</b> is 1.

### -field ConfigHostInverseScan

If the value is 1, the inverse scan for transform-domain block processing will be performed on the host, and absolute indices will be sent instead for any transform coefficients. If the value is 0, the inverse scan will be performed on the accelerator.
          

The value must be 0 if <b>ConfigResidDiffAccelerator</b> is 0 or if <b>Config4GroupedCoefs</b> is 1.

### -field ConfigSpecificIDCT

If the value is 1, the IDCT specified in Annex W of ITU-T Recommendation H.263 is used. If the value is 0, any compliant IDCT can be used for off-host IDCT.
          

The H.263 annex does not comply with the IDCT requirements of MPEG-2 corrigendum 2, so the value must not be 1 for use with MPEG-2 video.
          

The value must be 0 if <b>ConfigResidDiffAccelerator</b> is 0, indicating purely host-based residual difference decoding.

### -field Config4GroupedCoefs

If the value is 1, transform coefficients for off-host IDCT will be sent using the <a href="/windows-hardware/drivers/ddi/content/dxva/ns-dxva-_dxva_tcoef4group">DXVA_TCoef4Group</a> structure. If the value is 0, the <a href="/windows-hardware/drivers/ddi/content/dxva/ns-dxva-_dxva_tcoefsingle">DXVA_TCoefSingle</a> structure is used. The value must be 0 if <b>ConfigResidDiffAccelerator</b> is 0 or if <b>ConfigHostInverseScan</b> is 1.

### -field ConfigMinRenderTargetBuffCount

Specifies how many frames the decoder device processes at any one time.

### -field ConfigDecoderSpecific

Contains decoder-specific configuration information.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>