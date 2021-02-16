---
UID: NS:dxva2api._DXVA2_DecodeBufferDesc
title: DXVA2_DecodeBufferDesc (dxva2api.h)
description: Describes a buffer sent from a decoder to a DirectX Video Acceleration (DXVA) device.
helpviewer_keywords: ["DXVA2_BitStreamDateBufferType","DXVA2_DeblockingControlBufferType","DXVA2_DecodeBufferDesc","DXVA2_DecodeBufferDesc structure [Media Foundation]","DXVA2_FilmGrainBuffer","DXVA2_InverseQuantizationMatrixBufferType","DXVA2_MacroBlockControlBufferType","DXVA2_MotionVectorBuffer","DXVA2_PictureParametersBufferType","DXVA2_ResidualDifferenceBufferType","DXVA2_SliceControlBufferType","dxva2api/DXVA2_DecodeBufferDesc","eb17005a-035d-41cb-8f54-97b5d0f84736","mf.dxva2_decodebufferdesc"]
old-location: mf\dxva2_decodebufferdesc.htm
tech.root: mf
ms.assetid: eb17005a-035d-41cb-8f54-97b5d0f84736
ms.date: 12/05/2018
ms.keywords: DXVA2_BitStreamDateBufferType, DXVA2_DeblockingControlBufferType, DXVA2_DecodeBufferDesc, DXVA2_DecodeBufferDesc structure [Media Foundation], DXVA2_FilmGrainBuffer, DXVA2_InverseQuantizationMatrixBufferType, DXVA2_MacroBlockControlBufferType, DXVA2_MotionVectorBuffer, DXVA2_PictureParametersBufferType, DXVA2_ResidualDifferenceBufferType, DXVA2_SliceControlBufferType, dxva2api/DXVA2_DecodeBufferDesc, eb17005a-035d-41cb-8f54-97b5d0f84736, mf.dxva2_decodebufferdesc
req.header: dxva2api.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXVA2_DecodeBufferDesc
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_DecodeBufferDesc
 - dxva2api/_DXVA2_DecodeBufferDesc
 - DXVA2_DecodeBufferDesc
 - dxva2api/DXVA2_DecodeBufferDesc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_DecodeBufferDesc
---

# DXVA2_DecodeBufferDesc structure


## -description

Describes a buffer sent from a decoder to a DirectX Video Acceleration (DXVA) device.

## -struct-fields

### -field CompressedBufferType

Identifies the type of buffer passed to the accelerator. Must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_PictureParametersBufferType"></a><a id="dxva2_pictureparametersbuffertype"></a><a id="DXVA2_PICTUREPARAMETERSBUFFERTYPE"></a><dl>
<dt><b>DXVA2_PictureParametersBufferType</b></dt>
</dl>
</td>
<td width="60%">
Picture decoding parameter buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_MacroBlockControlBufferType"></a><a id="dxva2_macroblockcontrolbuffertype"></a><a id="DXVA2_MACROBLOCKCONTROLBUFFERTYPE"></a><dl>
<dt><b>DXVA2_MacroBlockControlBufferType</b></dt>
</dl>
</td>
<td width="60%">
Macroblock control command buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_ResidualDifferenceBufferType"></a><a id="dxva2_residualdifferencebuffertype"></a><a id="DXVA2_RESIDUALDIFFERENCEBUFFERTYPE"></a><dl>
<dt><b>DXVA2_ResidualDifferenceBufferType</b></dt>
</dl>
</td>
<td width="60%">
Residual difference block data buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_DeblockingControlBufferType"></a><a id="dxva2_deblockingcontrolbuffertype"></a><a id="DXVA2_DEBLOCKINGCONTROLBUFFERTYPE"></a><dl>
<dt><b>DXVA2_DeblockingControlBufferType</b></dt>
</dl>
</td>
<td width="60%">
Deblocking filter control command buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_InverseQuantizationMatrixBufferType"></a><a id="dxva2_inversequantizationmatrixbuffertype"></a><a id="DXVA2_INVERSEQUANTIZATIONMATRIXBUFFERTYPE"></a><dl>
<dt><b>DXVA2_InverseQuantizationMatrixBufferType</b></dt>
</dl>
</td>
<td width="60%">
Inverse quantization matrix buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_SliceControlBufferType"></a><a id="dxva2_slicecontrolbuffertype"></a><a id="DXVA2_SLICECONTROLBUFFERTYPE"></a><dl>
<dt><b>DXVA2_SliceControlBufferType</b></dt>
</dl>
</td>
<td width="60%">
Slice-control buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_BitStreamDateBufferType"></a><a id="dxva2_bitstreamdatebuffertype"></a><a id="DXVA2_BITSTREAMDATEBUFFERTYPE"></a><dl>
<dt><b>DXVA2_BitStreamDateBufferType</b></dt>
</dl>
</td>
<td width="60%">
Bitstream data buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_MotionVectorBuffer"></a><a id="dxva2_motionvectorbuffer"></a><a id="DXVA2_MOTIONVECTORBUFFER"></a><dl>
<dt><b>DXVA2_MotionVectorBuffer</b></dt>
</dl>
</td>
<td width="60%">
Motion vector buffer.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_FilmGrainBuffer"></a><a id="dxva2_filmgrainbuffer"></a><a id="DXVA2_FILMGRAINBUFFER"></a><dl>
<dt><b>DXVA2_FilmGrainBuffer</b></dt>
</dl>
</td>
<td width="60%">
Film grain synthesis data buffer.
              

</td>
</tr>
</table>

### -field BufferIndex

Reserved. Set to zero.

### -field DataOffset

Specifies the offset of the relevant data from the beginning of the buffer, in bytes. Currently this value must be zero.

### -field DataSize

Specifies the amount of relevant data in the buffer, in bytes. The location of the last byte of content in the buffer is <b>DataOffset</b> + <b>DataSize</b> − 1.

### -field FirstMBaddress

Specifies the macroblock address of the first macroblock in the buffer. The macroblock address is given in raster scan order.

### -field NumMBsInBuffer

Specifies the number of macroblocks of data in the buffer. This count includes skipped macroblocks. This value must be zero if the data buffer type is one of the following: picture decoding parameters, inverse-quantization matrix, AYUV, IA44/AI44, DPXD, Highlight, or DCCMD.

### -field Width

Reserved. Set to zero.

### -field Height

Reserved. Set to zero.

### -field Stride

Reserved. Set to zero.

### -field ReservedBits

Reserved. Set to zero.

### -field pvPVPState

Pointer to a byte array that contains an initialization vector (IV) for encrypted data. If the decode buffer does not contain encrypted data, set this member to <b>NULL</b>.
          If the decode buffer contains encrypted data, the contents of <b>pvPVPState</b> depends on the type of encryption. For <b>D3DCRYPTOTYPE_AES128_CTR</b>, the <b>pvPVPState</b> member points to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv">DXVA2_AES_CTR_IV</a> structure.

## -remarks

This structure corresponds closely to the <a href="/windows-hardware/drivers/ddi/content/dxva/ns-dxva-_dxva_bufferdescription">DXVA_BufferDescription</a> structure in DXVA 1, but some of the fields are no longer used in DXVA 2.

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>