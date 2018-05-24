---
UID: NF:dxva2api.IDirectXVideoDecoder.GetBuffer
title: IDirectXVideoDecoder::GetBuffer
author: windows-driver-content
description: Retrieves a pointer to a DirectX Video Acceleration (DXVA) decoder buffer.
old-location: mf\idirectxvideodecoder_getbuffer.htm
old-project: medfound
ms.assetid: db2d4818-8a96-461e-88c4-f25d3200d815
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DXVA2_BitStreamDateBufferType, DXVA2_DeblockingControlBufferType, DXVA2_FilmGrainBuffer, DXVA2_InverseQuantizationMatrixBufferType, DXVA2_MacroBlockControlBufferType, DXVA2_MotionVectorBuffer, DXVA2_PictureParametersBufferType, DXVA2_ResidualDifferenceBufferType, DXVA2_SliceControlBufferType, GetBuffer, GetBuffer method [Media Foundation], GetBuffer method [Media Foundation],IDirectXVideoDecoder interface, IDirectXVideoDecoder interface [Media Foundation],GetBuffer method, IDirectXVideoDecoder.GetBuffer, IDirectXVideoDecoder::GetBuffer, db2d4818-8a96-461e-88c4-f25d3200d815, dxva2api/IDirectXVideoDecoder::GetBuffer, mf.idirectxvideodecoder_getbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DXVA2_SurfaceType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva2api.h
api_name:
-	IDirectXVideoDecoder.GetBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoDecoder::GetBuffer


## -description



          Retrieves a pointer to a DirectX Video Acceleration (DXVA) decoder buffer.
        


## -parameters




### -param BufferType [in]

Type of buffer to retrieve. Use one of the following values.

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
 


### -param ppBuffer [out]

Receives a pointer to the start of the memory buffer.


### -param pBufferSize [out]

Receives the size of the buffer, in bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The method locks the Direct3D surface that contains the buffer. When you are done using the buffer, call <a href="https://msdn.microsoft.com/e828a8e0-b9ec-4b86-abea-cbd8e0fd3a90">IDirectXVideoDecoder::ReleaseBuffer</a> to unlock the surface.

This method might block if too many operations have been queued on the GPU. The method unblocks when a free buffer becomes available.




## -see-also




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/116c19a3-39be-4f96-969f-f3d62ed33a70">IDirectXVideoDecoder</a>
 

 

