---
UID: NF:dxva2api.DXVA2CreateVideoService
title: DXVA2CreateVideoService function (dxva2api.h)
description: Creates a DirectX Video Acceleration (DXVA) services object.
helpviewer_keywords: ["DXVA2CreateVideoService","DXVA2CreateVideoService function [Media Foundation]","dxva2api/DXVA2CreateVideoService","e62dbacb-f638-4307-ba56-88415d881fc9","mf.dxva2createvideoservice"]
old-location: mf\dxva2createvideoservice.htm
tech.root: mf
ms.assetid: e62dbacb-f638-4307-ba56-88415d881fc9
ms.date: 12/05/2018
ms.keywords: DXVA2CreateVideoService, DXVA2CreateVideoService function [Media Foundation], dxva2api/DXVA2CreateVideoService, e62dbacb-f638-4307-ba56-88415d881fc9, mf.dxva2createvideoservice
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
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXVA2CreateVideoService
 - dxva2api/DXVA2CreateVideoService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - DXVA2CreateVideoService
---

# DXVA2CreateVideoService function


## -description

Creates a DirectX Video Acceleration (DXVA) services object. Call this function if your application uses DXVA directly, without using DirectShow or Media Foundation.

## -parameters

### -param pDD

A pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface of a Direct3D device.

### -param riid

The interface identifier (IID) of the requested interface. Any of the following interfaces might be supported by the Direct3D device:
          

<ul>
<li>
<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice">IDirectXVideoAccelerationService</a>
</li>
<li>
<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice">IDirectXVideoDecoderService</a>
</li>
<li>
<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>
</li>
</ul>

### -param ppService

Receives a pointer to the interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>