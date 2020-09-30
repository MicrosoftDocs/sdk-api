---
UID: NF:dxva2api.IDirectXVideoMemoryConfiguration.SetSurfaceType
title: IDirectXVideoMemoryConfiguration::SetSurfaceType (dxva2api.h)
description: Sets the video surface type that a decoder will use for DirectX Video Acceleration (DVXA) 2.0.
helpviewer_keywords: ["06fe0072-1fe5-491f-b0b7-fc85ca731fe7","IDirectXVideoMemoryConfiguration interface [Media Foundation]","SetSurfaceType method","IDirectXVideoMemoryConfiguration.SetSurfaceType","IDirectXVideoMemoryConfiguration::SetSurfaceType","SetSurfaceType","SetSurfaceType method [Media Foundation]","SetSurfaceType method [Media Foundation]","IDirectXVideoMemoryConfiguration interface","dxva2api/IDirectXVideoMemoryConfiguration::SetSurfaceType","mf.idirectxvideomemoryconfiguration_setsurfacetype"]
old-location: mf\idirectxvideomemoryconfiguration_setsurfacetype.htm
tech.root: mf
ms.assetid: 06fe0072-1fe5-491f-b0b7-fc85ca731fe7
ms.date: 12/05/2018
ms.keywords: 06fe0072-1fe5-491f-b0b7-fc85ca731fe7, IDirectXVideoMemoryConfiguration interface [Media Foundation],SetSurfaceType method, IDirectXVideoMemoryConfiguration.SetSurfaceType, IDirectXVideoMemoryConfiguration::SetSurfaceType, SetSurfaceType, SetSurfaceType method [Media Foundation], SetSurfaceType method [Media Foundation],IDirectXVideoMemoryConfiguration interface, dxva2api/IDirectXVideoMemoryConfiguration::SetSurfaceType, mf.idirectxvideomemoryconfiguration_setsurfacetype
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
 - IDirectXVideoMemoryConfiguration::SetSurfaceType
 - dxva2api/IDirectXVideoMemoryConfiguration::SetSurfaceType
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
 - IDirectXVideoMemoryConfiguration.SetSurfaceType
---

# IDirectXVideoMemoryConfiguration::SetSurfaceType


## -description

Sets the video surface type that a decoder will use for DirectX Video Acceleration (DVXA) 2.0.

## -parameters

### -param dwType [in]

Member of the <a href="/windows/win32/api/dxva2api/ne-dxva2api-dxva2_surfacetype">DXVA2_SurfaceType</a> enumeration specifying the surface type. Currently, the only supported value is DXVA2_SurfaceType_DecoderRenderTarget.

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
<dt><b>ERROR_UNSUPPORTED_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The renderer does not support the specified surface type.

</td>
</tr>
</table>

## -remarks

By calling this method, the caller agrees to create surfaces of the type specified in the <i>dwType</i> parameter.

In DirectShow, during pin connection, a video decoder that supports DVXA 2.0 should call <b>SetSurface</b> with the value DXVA2_SurfaceType_DecoderRenderTarget. This notifies the video renderer that the decoder will provide the allocator and will create the Direct3D surfaces for decoding. For more information, see <a href="/windows/desktop/medfound/supporting-dxva-2-0-in-directshow">Supporting DXVA 2.0 in DirectShow</a>.

The only way to undo the setting is to break the pin connection.

## -see-also

<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration">IDirectXVideoMemoryConfiguration</a>



<a href="/windows/desktop/medfound/supporting-dxva-2-0-in-directshow">Supporting DXVA 2.0 in DirectShow</a>