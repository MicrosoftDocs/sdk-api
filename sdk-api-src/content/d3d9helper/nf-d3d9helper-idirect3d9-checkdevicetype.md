---
UID: NF:d3d9helper.IDirect3D9.CheckDeviceType
title: IDirect3D9::CheckDeviceType (d3d9helper.h)
description: The IDirect3D9::CheckDeviceType (d3d9helper.h) method verifies whether a hardware accelerated device type can be used on this adapter.
helpviewer_keywords: ["74a3aa81-9498-9ce0-0ae8-0bc9d18d553b","CheckDeviceType","CheckDeviceType method [Direct3D 9]","CheckDeviceType method [Direct3D 9]","IDirect3D9 interface","IDirect3D9 interface [Direct3D 9]","CheckDeviceType method","IDirect3D9.CheckDeviceType","IDirect3D9::CheckDeviceType","d3d9helper/IDirect3D9::CheckDeviceType","direct3d9.idirect3d9__checkdevicetype"]
old-location: direct3d9\idirect3d9__checkdevicetype.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__checkdevicetype.htm
ms.date: 08/11/2022
ms.keywords: 74a3aa81-9498-9ce0-0ae8-0bc9d18d553b, CheckDeviceType, CheckDeviceType method [Direct3D 9], CheckDeviceType method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],CheckDeviceType method, IDirect3D9.CheckDeviceType, IDirect3D9::CheckDeviceType, d3d9helper/IDirect3D9::CheckDeviceType, direct3d9.idirect3d9__checkdevicetype
req.header: d3d9helper.h
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
 - IDirect3D9::CheckDeviceType
 - d3d9helper/IDirect3D9::CheckDeviceType
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
 - IDirect3D9.CheckDeviceType
---

# IDirect3D9::CheckDeviceType


## -description

Verifies whether a hardware accelerated device type can be used on this adapter.

## -parameters

### -param iAdapter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number denoting the display adapter to enumerate. D3DADAPTER_DEFAULT is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system.

### -param DevType [in]

Type: <b><a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3ddevtype">D3DDEVTYPE</a> enumerated type, indicating the device type to check.

### -param DisplayFormat

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Member of the <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> enumerated type, indicating the format of the adapter display mode for which the device type is to be checked. For example, some devices will operate only in 16-bits-per-pixel modes.

### -param BackBufferFormat [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a></b>

Back buffer format. For more information about formats, see <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a>. This value must be one of the render-target formats. You can use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode">GetAdapterDisplayMode</a> to obtain the current format.
    
 For windowed applications, the back buffer format does not need to match the display mode format if the hardware supports color conversion. The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format. There is the additional requirement that the device be operable in the desktop because devices typically do not operate in 8 bits per pixel modes.
    
 Full-screen applications cannot do color conversion.
    
 D3DFMT_UNKNOWN is allowed for windowed mode.

### -param bWindowed [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Value indicating whether the device type will be used in full-screen or windowed mode. If set to <b>TRUE</b>, the query is performed for windowed applications; otherwise, this value should be set <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the device can be used on this adapter, D3D_OK is returned.

 D3DERR_INVALIDCALL is returned if Adapter equals or exceeds the number of display adapters in the system. D3DERR_INVALIDCALL is also returned if <b>CheckDeviceType</b> specified a device that does not exist.

 D3DERR_NOTAVAILABLE is returned if the requested back buffer format is not supported, or if hardware acceleration is not available for the specified formats.

## -remarks

A hal device type requires hardware acceleration. Applications can use CheckDeviceType to determine if the needed hardware and drivers are present to support a hal device. 

Full-screen applications should not specify a DisplayFormat that contains an alpha channel. This will result in a failed call. Note that an alpha channel can be present in the back buffer but the two display formats must be identical in all other respects. For example, if DisplayFormat = D3DFMT_X1R5G5B5, valid values for BackBufferFormat include D3DFMT_X1R5G5B5 and D3DFMT_A1R5G5B5 but exclude D3DFMT_R5G6B5.

The following code fragment shows how you could use CheckDeviceType to test whether a certain device type can be used on this adapter.


```

if(SUCCEEDED(pD3Device->CheckDeviceType(D3DADAPTER_DEFAULT, 
                                        D3DDEVTYPE_HAL, 
                                        DisplayFormat, 
                                        BackBufferFormat, 
                                        bIsWindowed)))
    
     return S_OK;
// There is no HAL on this adapter using this render-target format. 
// Try again, using another format.

```


This code returns S_OK if the device can be used on the default adapter with the specified surface format.

Using <b>CheckDeviceType</b> to test for compatibility between a back buffer that differs from the display format will return appropriate values. This means that the call will reflect device capabilities. If the device cannot render to the requested back-buffer format, the call will still return D3DERR_NOTAVAILABLE. If the device can render to the format, but cannot perform the color-converting presentation, the return value will also be D3DERR_NOTAVAILABLE. Applications can discover hardware support for the presentation itself by calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformatconversion">CheckDeviceFormatConversion</a>. No software emulation for the color-converting presentation itself will be offered.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>
