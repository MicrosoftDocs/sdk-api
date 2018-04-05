---
UID: NF:dxva2api.IDirectXVideoDecoderService.GetDecoderDeviceGuids
title: IDirectXVideoDecoderService::GetDecoderDeviceGuids method
author: windows-driver-content
description: Retrieves an array of GUIDs that identifies the decoder devices supported by the graphics hardware.
old-location: mf\idirectxvideodecoderservice_getdecoderdeviceguids.htm
old-project: medfound
ms.assetid: 53980b1f-2be1-4267-a581-a4b09255b89f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 53980b1f-2be1-4267-a581-a4b09255b89f, GetDecoderDeviceGuids method [Media Foundation], GetDecoderDeviceGuids method [Media Foundation], IDirectXVideoDecoderService interface, GetDecoderDeviceGuids,IDirectXVideoDecoderService.GetDecoderDeviceGuids, IDirectXVideoDecoderService, IDirectXVideoDecoderService interface [Media Foundation], GetDecoderDeviceGuids method, IDirectXVideoDecoderService::GetDecoderDeviceGuids, dxva2api/IDirectXVideoDecoderService::GetDecoderDeviceGuids, mf.idirectxvideodecoderservice_getdecoderdeviceguids
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
-	IDirectXVideoDecoderService.GetDecoderDeviceGuids
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoDecoderService::GetDecoderDeviceGuids method


## -description



Retrieves an array of GUIDs that identifies the decoder devices supported by the graphics hardware.




## -parameters




### -param pCount




### -param pGuids [out]

Receives an array of GUIDs. The size of the array is retrieved in the <i>Count</i> parameter. The method allocates the memory for the array. The caller must free the memory by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


#### - Count [out]

Receives the number of GUIDs.


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




<a href="https://msdn.microsoft.com/acb73b20-89fa-4a48-be4a-846715a239b0">DirectX Video Acceleration 2.0</a>



<a href="https://msdn.microsoft.com/eeb62178-b54d-45d3-a584-75865f0662fa">IDirectXVideoDecoderService</a>
 

 

