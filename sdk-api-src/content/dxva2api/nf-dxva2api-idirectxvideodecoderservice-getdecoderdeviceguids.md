---
UID: NF:dxva2api.IDirectXVideoDecoderService.GetDecoderDeviceGuids
title: IDirectXVideoDecoderService::GetDecoderDeviceGuids (dxva2api.h)
description: Retrieves an array of GUIDs that identifies the decoder devices supported by the graphics hardware.
helpviewer_keywords: ["53980b1f-2be1-4267-a581-a4b09255b89f","GetDecoderDeviceGuids","GetDecoderDeviceGuids method [Media Foundation]","GetDecoderDeviceGuids method [Media Foundation]","IDirectXVideoDecoderService interface","IDirectXVideoDecoderService interface [Media Foundation]","GetDecoderDeviceGuids method","IDirectXVideoDecoderService.GetDecoderDeviceGuids","IDirectXVideoDecoderService::GetDecoderDeviceGuids","dxva2api/IDirectXVideoDecoderService::GetDecoderDeviceGuids","mf.idirectxvideodecoderservice_getdecoderdeviceguids"]
old-location: mf\idirectxvideodecoderservice_getdecoderdeviceguids.htm
tech.root: mf
ms.assetid: 53980b1f-2be1-4267-a581-a4b09255b89f
ms.date: 12/05/2018
ms.keywords: 53980b1f-2be1-4267-a581-a4b09255b89f, GetDecoderDeviceGuids, GetDecoderDeviceGuids method [Media Foundation], GetDecoderDeviceGuids method [Media Foundation],IDirectXVideoDecoderService interface, IDirectXVideoDecoderService interface [Media Foundation],GetDecoderDeviceGuids method, IDirectXVideoDecoderService.GetDecoderDeviceGuids, IDirectXVideoDecoderService::GetDecoderDeviceGuids, dxva2api/IDirectXVideoDecoderService::GetDecoderDeviceGuids, mf.idirectxvideodecoderservice_getdecoderdeviceguids
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectXVideoDecoderService::GetDecoderDeviceGuids
 - dxva2api/IDirectXVideoDecoderService::GetDecoderDeviceGuids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoDecoderService.GetDecoderDeviceGuids
---

# IDirectXVideoDecoderService::GetDecoderDeviceGuids


## -description

Retrieves an array of GUIDs that identifies the decoder devices supported by the graphics hardware.

## -parameters

### -param pCount [out]

Receives the number of GUIDs.

### -param pGuids [out]

Receives an array of GUIDs. The size of the array is retrieved in the <i>Count</i> parameter. The method allocates the memory for the array. The caller must free the memory by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>D3DERR_INVALIDCALL</b></dt>
</dl>
</td>
<td width="60%">
Error from the Direct3D device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
If the Microsoft Basic Display Adapter is being used or the Direct3D 11 device type is the reference rasterizer.  These devices do not support video decoders.

</td>
</tr>
</table>

## -remarks

The following decoder GUIDs are defined. Some of these GUIDs have alternate names, shown in parentheses.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td>DXVA2_ModeH264_A (DXVA2_ModeH264_MoComp_NoFGT)</td>
<td>H.264 motion compensation (MoComp), no film grain technology (FGT).</td>
</tr>
<tr>
<td>DXVA2_ModeH264_B (DXVA2_ModeH264_MoComp_FGT)</td>
<td>H.264 MoComp, FGT.</td>
</tr>
<tr>
<td>DXVA2_ModeH264_C (DXVA2_ModeH264_IDCT_NoFGT)</td>
<td>H.264 inverse discrete cosine transform (IDCT), no FGT.</td>
</tr>
<tr>
<td>DXVA2_ModeH264_D (DXVA2_ModeH264_IDCT_FGT)</td>
<td>H.264 IDCT, FGT.</td>
</tr>
<tr>
<td>DXVA2_ModeH264_E (DXVA2_ModeH264_VLD_NoFGT)</td>
<td>H.264 VLD, no FGT.</td>
</tr>
<tr>
<td>DXVA2_ModeH264_F (DXVA2_ModeH264_VLD_FGT)</td>
<td>H.264 variable-length decoder (VLD), FGT.</td>
</tr>
<tr>
<td>DXVA2_ModeHEVC_VLD_Main</td>
<td>H.265 / HEVC Main profile</td>
</tr>
<tr>
<td>DXVA2_ModeHEVC_VLD_Main10</td>
<td>H.265 / HEVC Main 10 profile</td>
</tr>
<tr>
<td>DXVA2_ModeMPEG2_IDCT</td>
<td>MPEG-2 IDCT.</td>
</tr>
<tr>
<td>DXVA2_ModeMPEG2_MoComp</td>
<td>MPEG-2 MoComp.</td>
</tr>
<tr>
<td>DXVA2_ModeMPEG2_VLD</td>
<td>MPEG-2 VLD.</td>
</tr>
<tr>
<td>DXVA2_ModeVC1_A (DXVA2_ModeVC1_PostProc)</td>
<td>VC-1 post processing.</td>
</tr>
<tr>
<td>DXVA2_ModeVC1_B (DXVA2_ModeVC1_MoComp)</td>
<td>VC-1 MoComp.</td>
</tr>
<tr>
<td>DXVA2_ModeVC1_C (DXVA2_ModeVC1_IDCT)</td>
<td>VC-1 IDCT.</td>
</tr>
<tr>
<td>DXVA2_ModeVC1_D (DXVA2_ModeVC1_VLD)</td>
<td>VC-1 VLD.</td>
</tr>
<tr>
<td>DXVA2_ModeWMV8_A (DXVA2_ModeWMV8_PostProc)</td>
<td>Windows Media Video 8 post processing.</td>
</tr>
<tr>
<td>DXVA2_ModeWMV8_B (DXVA2_ModeWMV8_MoComp)</td>
<td>Windows Media Video 8 MoComp.</td>
</tr>
<tr>
<td>DXVA2_ModeWMV9_A (DXVA2_ModeWMV9_PostProc)</td>
<td>Windows Media Video 9 post processing.</td>
</tr>
<tr>
<td>DXVA2_ModeWMV9_B (DXVA2_ModeWMV9_MoComp)</td>
<td>Windows Media Video 9 MoComp.</td>
</tr>
<tr>
<td>DXVA2_ModeWMV9_C (DXVA2_ModeWMV9_IDCT)</td>
<td>Windows Media Video 9 IDCT.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice">IDirectXVideoDecoderService</a>