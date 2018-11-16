---
UID: NF:dxva2api.IDirectXVideoMemoryConfiguration.SetSurfaceType
title: IDirectXVideoMemoryConfiguration::SetSurfaceType
author: windows-sdk-content
description: Sets the video surface type that a decoder will use for DirectX Video Acceleration (DVXA) 2.0.
old-location: mf\idirectxvideomemoryconfiguration_setsurfacetype.htm
tech.root: medfound
ms.assetid: 06fe0072-1fe5-491f-b0b7-fc85ca731fe7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 06fe0072-1fe5-491f-b0b7-fc85ca731fe7, IDirectXVideoMemoryConfiguration interface [Media Foundation],SetSurfaceType method, IDirectXVideoMemoryConfiguration.SetSurfaceType, IDirectXVideoMemoryConfiguration::SetSurfaceType, SetSurfaceType, SetSurfaceType method [Media Foundation], SetSurfaceType method [Media Foundation],IDirectXVideoMemoryConfiguration interface, dxva2api/IDirectXVideoMemoryConfiguration::SetSurfaceType, mf.idirectxvideomemoryconfiguration_setsurfacetype
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoMemoryConfiguration.SetSurfaceType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxva2api.h
: 
- IDirectXVideoMemoryConfiguration.SetSurfaceType
: 
---

# IDirectXVideoMemoryConfiguration::SetSurfaceType


## -description



Sets the video surface type that a decoder will use for DirectX Video Acceleration (DVXA) 2.0.




## -parameters




### -param dwType [in]

Member of the <a href="https://msdn.microsoft.com/7ede2247-7878-4b70-9a74-56b626013989">DXVA2_SurfaceType</a> enumeration specifying the surface type. Currently, the only supported value is DXVA2_SurfaceType_DecoderRenderTarget.


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

In DirectShow, during pin connection, a video decoder that supports DVXA 2.0 should call <b>SetSurface</b> with the value DXVA2_SurfaceType_DecoderRenderTarget. This notifies the video renderer that the decoder will provide the allocator and will create the Direct3D surfaces for decoding. For more information, see <a href="https://msdn.microsoft.com/40deaddb-bb17-4a34-8294-5c7dc8a8a457">Supporting DXVA 2.0 in DirectShow</a>.

The only way to undo the setting is to break the pin connection.




## -see-also




<a href="https://msdn.microsoft.com/cc2a6180-9698-460a-9a0d-1ee9e15f197f">IDirectXVideoMemoryConfiguration</a>



<a href="https://msdn.microsoft.com/40deaddb-bb17-4a34-8294-5c7dc8a8a457">Supporting DXVA 2.0 in DirectShow</a>
 

 

