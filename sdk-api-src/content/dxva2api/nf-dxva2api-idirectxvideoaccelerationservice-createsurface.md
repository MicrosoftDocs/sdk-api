---
UID: NF:dxva2api.IDirectXVideoAccelerationService.CreateSurface
title: IDirectXVideoAccelerationService::CreateSurface (dxva2api.h)
description: Creates a DirectX Video Acceleration (DXVA) video processor or DXVA decoder render target.
helpviewer_keywords: ["34ed2029-7c79-45ce-962d-df4970babb23","CreateSurface","CreateSurface method [Media Foundation]","CreateSurface method [Media Foundation]","IDirectXVideoAccelerationService interface","DXVA2_VideoDecoderRenderTarget","DXVA2_VideoProcessorRenderTarget","DXVA2_VideoSoftwareRenderTarget","IDirectXVideoAccelerationService interface [Media Foundation]","CreateSurface method","IDirectXVideoAccelerationService.CreateSurface","IDirectXVideoAccelerationService::CreateSurface","dxva2api/IDirectXVideoAccelerationService::CreateSurface","mf.idirectxvideoaccelerationservice_createsurface"]
old-location: mf\idirectxvideoaccelerationservice_createsurface.htm
tech.root: mf
ms.assetid: 34ed2029-7c79-45ce-962d-df4970babb23
ms.date: 12/05/2018
ms.keywords: 34ed2029-7c79-45ce-962d-df4970babb23, CreateSurface, CreateSurface method [Media Foundation], CreateSurface method [Media Foundation],IDirectXVideoAccelerationService interface, DXVA2_VideoDecoderRenderTarget, DXVA2_VideoProcessorRenderTarget, DXVA2_VideoSoftwareRenderTarget, IDirectXVideoAccelerationService interface [Media Foundation],CreateSurface method, IDirectXVideoAccelerationService.CreateSurface, IDirectXVideoAccelerationService::CreateSurface, dxva2api/IDirectXVideoAccelerationService::CreateSurface, mf.idirectxvideoaccelerationservice_createsurface
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
 - IDirectXVideoAccelerationService::CreateSurface
 - dxva2api/IDirectXVideoAccelerationService::CreateSurface
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
 - IDirectXVideoAccelerationService.CreateSurface
---

# IDirectXVideoAccelerationService::CreateSurface


## -description

Creates a DirectX Video Acceleration (DXVA) video processor or DXVA decoder render target.

## -parameters

### -param Width [in]

The width of the surface, in pixels.

### -param Height [in]

The height of the surface, in pixels.

### -param BackBuffers [in]

The number of back buffers. The method creates <i>BackBuffers</i> + 1 surfaces.

### -param Format [in]

The pixel format, specified as a <b>D3DFORMAT</b> value or FOURCC code. For more information, see the Direct3D documentation.

### -param Pool [in]

The memory pool in which to create the surface, specified as a <b>D3DPOOL</b> value. For more information, see the Direct3D documentation. Decoders should generally use the value D3DPOOL_DEFAULT.

### -param Usage [in]

Reserved. Set this value to zero.

### -param DxvaType [in]

The type of surface to create. Use one of the following values.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoDecoderRenderTarget"></a><a id="dxva2_videodecoderrendertarget"></a><a id="DXVA2_VIDEODECODERRENDERTARGET"></a><dl>
<dt><b>DXVA2_VideoDecoderRenderTarget</b></dt>
</dl>
</td>
<td width="60%">
Video decoder render target.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoProcessorRenderTarget"></a><a id="dxva2_videoprocessorrendertarget"></a><a id="DXVA2_VIDEOPROCESSORRENDERTARGET"></a><dl>
<dt><b>DXVA2_VideoProcessorRenderTarget</b></dt>
</dl>
</td>
<td width="60%">
Video processor render target. Used for <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt">IDirectXVideoProcessor::VideoProcessBlt</a> operations.
              

</td>
</tr>
<tr>
<td width="40%"><a id="DXVA2_VideoSoftwareRenderTarget"></a><a id="dxva2_videosoftwarerendertarget"></a><a id="DXVA2_VIDEOSOFTWARERENDERTARGET"></a><dl>
<dt><b>DXVA2_VideoSoftwareRenderTarget</b></dt>
</dl>
</td>
<td width="60%">
Software render target. This surface type is for use with software DXVA devices.
              

</td>
</tr>
</table>

### -param ppSurface [out]

The address of an array of <b>IDirect3DSurface9</b> pointers allocated by the caller. The size of the array must be 1 + <i>BackBuffers</i> (enough for the back buffers plus one front buffer). The method fills the array with <b>IDirect3DSurface9</b> pointers. The caller must release all of the interface pointers. In addition, the front buffer holds a reference count on each of the back buffers. Therefore, the back buffers are never deleted until the front buffer is deleted.

### -param pSharedHandle [in, out]

A pointer to a handle that is used to share the surfaces between Direct3D devices. Set this parameter to <b>NULL</b>.

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
Invalid parameter
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The DirectX Video Acceleration Manager is not initialized.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.
              

</td>
</tr>
</table>

## -remarks

If the method returns <b>E_FAIL</b>, try calling <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice">IDirect3DDeviceManager9::ResetDevice</a> to reset the DirectX Video Acceleration Manager.

## -see-also

<a href="/windows/desktop/medfound/directx-video-acceleration-2-0">DirectX Video Acceleration 2.0</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>