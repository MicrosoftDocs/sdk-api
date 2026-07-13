---
UID: NF:d3d9.IDirect3D9.CheckDepthStencilMatch
title: IDirect3D9::CheckDepthStencilMatch (d3d9.h)
description: The IDirect3D9::CheckDepthStencilMatch method (d3d9helper.h) determines whether a depth-stencil format is compatible with a render-target format in a particular display mode. 
helpviewer_keywords: ["64b8e751-080a-bbb1-2461-2c51a5600a61","CheckDepthStencilMatch","CheckDepthStencilMatch method [Direct3D 9]","CheckDepthStencilMatch method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","CheckDepthStencilMatch method","IDirect3D9.CheckDepthStencilMatch","IDirect3D9::CheckDepthStencilMatch","d3d9helper/IDirect3D9::CheckDepthStencilMatch","direct3d9.idirect3d9__checkdepthstencilmatch"]
old-location: direct3d9\idirect3d9__checkdepthstencilmatch.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__checkdepthstencilmatch.htm
ms.date: 08/10/2022
ms.keywords: 64b8e751-080a-bbb1-2461-2c51a5600a61, CheckDepthStencilMatch, CheckDepthStencilMatch method [Direct3D 9], CheckDepthStencilMatch method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],CheckDepthStencilMatch method, IDirect3D9.CheckDepthStencilMatch, IDirect3D9::CheckDepthStencilMatch, d3d9helper/IDirect3D9::CheckDepthStencilMatch, direct3d9.idirect3d9__checkdepthstencilmatch
req.header: d3d9.h
req.include-header: D3D9.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3D9::CheckDepthStencilMatch
 - d3d9/IDirect3D9::CheckDepthStencilMatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9.CheckDepthStencilMatch
---

# IDirect3D9::CheckDepthStencilMatch


## -description

Determines whether a depth-stencil format is compatible with a render-target format in a particular display mode.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number denoting the display adapter to query. D3DADAPTER_DEFAULT is always the primary display adapter.

### -param DeviceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a> enumerated type, identifying the device type.

### -param AdapterFormat [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, identifying the format of the display mode into which the adapter will be placed.

### -param RenderTargetFormat [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, identifying the format of the render-target surface to be tested.

### -param DepthStencilFormat [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, identifying the format of the depth-stencil surface to be tested.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the depth-stencil format is compatible with the render-target format in the display mode, this method returns D3D_OK. D3DERR_INVALIDCALL can be returned if one or more of the parameters is invalid. If a depth-stencil format is not compatible with the render target in the display mode, then this method returns D3DERR_NOTAVAILABLE.

## -remarks

This method is provided to enable applications to work with hardware requiring that certain depth formats can only work with certain render-target formats.

The behavior of this method has been changed for DirectX 8.1.  This method now pays attention to the D24x8 and D32 depth-stencil formats. The previous version assumed that these formats would always be usable with 32- or 16-bit render targets. This method will now return D3D_OK for these formats only if the device is capable of mixed-depth operations.

The following code fragment shows how you could use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat">CheckDeviceFormat</a> to validate a depth stencil format.


```

BOOL IsDepthFormatOk(D3DFORMAT DepthFormat, 
                          D3DFORMAT AdapterFormat, 
                          D3DFORMAT BackBufferFormat)
{
    
    // Verify that the depth format exists
    HRESULT hr = pD3D->CheckDeviceFormat(D3DADAPTER_DEFAULT,
                                         D3DDEVTYPE_HAL,
                                         AdapterFormat,
                                         D3DUSAGE_DEPTHSTENCIL,
                                         D3DRTYPE_SURFACE,
                                         DepthFormat);
    
    if(FAILED(hr)) return FALSE;
    
    // Verify that the depth format is compatible
    hr = pD3D->CheckDepthStencilMatch(D3DADAPTER_DEFAULT,
                                      D3DDEVTYPE_HAL,
                                      AdapterFormat,
                                      BackBufferFormat,
                                      DepthFormat);
    
    return SUCCEEDED(hr);
    
}

```


The preceding call will return <b>FALSE</b> if DepthFormat cannot be used in conjunction with AdapterFormat and BackBufferFormat.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
