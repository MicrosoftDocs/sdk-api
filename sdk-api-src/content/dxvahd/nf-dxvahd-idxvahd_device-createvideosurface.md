---
UID: NF:dxvahd.IDXVAHD_Device.CreateVideoSurface
title: IDXVAHD_Device::CreateVideoSurface (dxvahd.h)
description: Creates one or more Microsoft Direct3D video surfaces.
helpviewer_keywords: ["CreateVideoSurface","CreateVideoSurface method [Media Foundation]","CreateVideoSurface method [Media Foundation]","IDXVAHD_Device interface","IDXVAHD_Device interface [Media Foundation]","CreateVideoSurface method","IDXVAHD_Device.CreateVideoSurface","IDXVAHD_Device::CreateVideoSurface","dxvahd/IDXVAHD_Device::CreateVideoSurface","mf.idxvahd_device_createvideosurface"]
old-location: mf\idxvahd_device_createvideosurface.htm
tech.root: mf
ms.assetid: c467a077-104c-443d-896b-d69441aa5160
ms.date: 12/05/2018
ms.keywords: CreateVideoSurface, CreateVideoSurface method [Media Foundation], CreateVideoSurface method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],CreateVideoSurface method, IDXVAHD_Device.CreateVideoSurface, IDXVAHD_Device::CreateVideoSurface, dxvahd/IDXVAHD_Device::CreateVideoSurface, mf.idxvahd_device_createvideosurface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXVAHD_Device::CreateVideoSurface
 - dxvahd/IDXVAHD_Device::CreateVideoSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.CreateVideoSurface
---

# IDXVAHD_Device::CreateVideoSurface


## -description

Creates one or more Microsoft Direct3D video surfaces.

## -parameters

### -param Width [in]

The width of each surface, in pixels.

### -param Height [in]

The height of each surface, in pixels.

### -param Format [in]

The pixel format, specified as a <b>D3DFORMAT</b> value or FOURCC code. For more information, see <a href="/windows/desktop/medfound/video-fourccs">Video FOURCCs</a>.

### -param Pool [in]

The memory pool in which the surface is  created. This parameter must equal the <b>InputPool</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. Call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method to get this value.

### -param Usage [in]

Reserved. Set to 0.

### -param Type [in]

The type of surface to create, specified as a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_surface_type">DXVAHD_SURFACE_TYPE</a> enumeration.

### -param NumSurfaces [in]

The number of surfaces to create.

### -param ppSurfaces [out]

A pointer to an array of <b>IDirect3DSurface9</b> pointers. The <i>NumSurfaces</i> parameter specifies the number of elements in the array. The method fills the array with pointers to the new video surfaces. The caller must release the pointers.

### -param pSharedHandle [in, out]

Reserved. Set to <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a>