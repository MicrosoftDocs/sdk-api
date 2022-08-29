---
UID: NF:d3d9.IDirect3D9.CheckDeviceFormat
title: IDirect3D9::CheckDeviceFormat (d3d9.h)
description: The IDirect3D9::CheckDeviceFormat method (d3d9helper.h) determines whether a surface format is available as a specified resource type. 
helpviewer_keywords: ["CheckDeviceFormat","CheckDeviceFormat method [Direct3D 9]","CheckDeviceFormat method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","CheckDeviceFormat method","IDirect3D9.CheckDeviceFormat","IDirect3D9::CheckDeviceFormat","d3d9helper/IDirect3D9::CheckDeviceFormat","daa5cafd-0b8b-a747-98fe-eb9db7acde6d","direct3d9.idirect3d9__checkdeviceformat"]
old-location: direct3d9\idirect3d9__checkdeviceformat.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__checkdeviceformat.htm
ms.date: 08/10/2022
ms.keywords: CheckDeviceFormat, CheckDeviceFormat method [Direct3D 9], CheckDeviceFormat method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],CheckDeviceFormat method, IDirect3D9.CheckDeviceFormat, IDirect3D9::CheckDeviceFormat, d3d9helper/IDirect3D9::CheckDeviceFormat, daa5cafd-0b8b-a747-98fe-eb9db7acde6d, direct3d9.idirect3d9__checkdeviceformat
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
 - IDirect3D9::CheckDeviceFormat
 - d3d9/IDirect3D9::CheckDeviceFormat
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
 - IDirect3D9.CheckDeviceFormat
---

# IDirect3D9::CheckDeviceFormat


## -description

Determines whether a surface format is available as a specified resource type and can be used as a texture, depth-stencil buffer, or render target, or any combination of the three, on a device representing this adapter.

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number denoting the display adapter to query. <a href="/windows/desktop/direct3d9/d3dadapter-default">D3DADAPTER_DEFAULT</a> is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system.

### -param DeviceType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a> enumerated type, identifying the device type.

### -param AdapterFormat [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, identifying the format of the display mode into which the adapter will be placed.

### -param Usage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Requested usage options for the surface. Usage options are any combination of <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE</a> and <a href="/windows/desktop/direct3d9/d3dusage-query">D3DUSAGE_QUERY</a> constants (only a subset of the D3DUSAGE constants are valid for <b>CheckDeviceFormat</b>; see the table on the D3DUSAGE page).

### -param RType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dresourcetype">D3DRESOURCETYPE</a></b>

Resource type requested for use with the queried format. Member of <a href="/windows/desktop/direct3d9/d3dresourcetype">D3DRESOURCETYPE</a>.

### -param CheckFormat [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Format of the surfaces which may be used, as defined by Usage. Member of <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the format is compatible with the specified device for the requested usage, this method returns D3D_OK.

D3DERR_INVALIDCALL is returned if Adapter equals or exceeds the number of display adapters in the system, or if DeviceType is unsupported.

D3DERR_NOTAVAILABLE is returned if the format is not acceptable to the device for this usage.

## -remarks

Here are some examples using <b>CheckDeviceFormat</b> to check for hardware support of:

<ul>
<li>An off-screen plain surface format - Specify Usage = 0 and RType = D3DRTYPE_SURFACE.</li>
<li>A depth-stencil format - The following snippet tests for the passed in depth-stencil format:
    

```

BOOL IsDepthFormatExisting( D3DFORMAT DepthFormat, D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          D3DUSAGE_DEPTHSTENCIL,
                                          D3DRTYPE_SURFACE,
                                          DepthFormat);
    
    return SUCCEEDED( hr );
}
```


See <a href="/windows/desktop/direct3d9/selecting-a-device">Selecting a Device (Direct3D 9)</a> for more detail on the enumeration process.

</li>
<li>Can this texture be rendered in a particular format - Given the current display mode, this example shows how to verify that the texture format is compatible with the specific back-buffer format:
    
    
    

```

BOOL IsTextureFormatOk( D3DFORMAT TextureFormat, D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);
    
    return SUCCEEDED( hr );
}
```


</li>
<li>Alpha blending in a pixel shader - Set Usage to <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE_QUERY_POSTPIXELSHADER_BLENDING</a>. Expect this to fail for all floating-point render targets.</li>
<li>Autogeneration of mipmaps - Set Usage to <a href="/windows/desktop/direct3d9/d3dusage">D3DUSAGE_AUTOGENMIPMAP</a>. If the mipmap automatic generation fails, the application will get a non-mipmapped texture. Calling this method is considered a hint, so this method can return D3DOK_NOAUTOGEN (a valid success code) if the only thing that fails is the mipmap generation. For more information about mipmap generation, see <a href="/windows/desktop/direct3d9/automatic-generation-of-mipmaps">Automatic Generation of Mipmaps (Direct3D 9)</a>.</li>
</ul>
When migrating code from Direct3D 9 to Direct3D 10, the Direct3D 10 equivalent to CheckDeviceFormat is <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkformatsupport">CheckFormatSupport</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
