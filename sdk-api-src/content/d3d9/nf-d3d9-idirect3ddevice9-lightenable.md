---
UID: NF:d3d9.IDirect3DDevice9.LightEnable
title: IDirect3DDevice9::LightEnable (d3d9.h)
description: The IDirect3DDevice9::LightEnable method (d3d9.h) enables or disables a set of lighting parameters within a device.
helpviewer_keywords: ["93cddc72-1451-3e41-6d33-7b1036dfc225","IDirect3DDevice9 interface [Direct3D 9]","LightEnable method","IDirect3DDevice9.LightEnable","IDirect3DDevice9::LightEnable","LightEnable","LightEnable method [Direct3D 9]","LightEnable method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::LightEnable","direct3d9.idirect3ddevice9__lightenable"]
old-location: direct3d9\idirect3ddevice9__lightenable.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__lightenable.htm
ms.date: 08/11/2022
ms.keywords: 93cddc72-1451-3e41-6d33-7b1036dfc225, IDirect3DDevice9 interface [Direct3D 9],LightEnable method, IDirect3DDevice9.LightEnable, IDirect3DDevice9::LightEnable, LightEnable, LightEnable method [Direct3D 9], LightEnable method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::LightEnable, direct3d9.idirect3ddevice9__lightenable
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
 - IDirect3DDevice9::LightEnable
 - d3d9/IDirect3DDevice9::LightEnable
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
 - IDirect3DDevice9.LightEnable
---

# IDirect3DDevice9::LightEnable


## -description

Enables or disables a set of lighting parameters within a device.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Zero-based index of the set of lighting parameters that are the target of this method.

### -param Enable [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Value that indicates if the set of lighting parameters are being enabled or disabled. Set this parameter to <b>TRUE</b> to enable lighting with the parameters at the specified index, or <b>FALSE</b> to disable it.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

If a value for LightIndex is outside the range of the light property sets assigned within the device, the <b>IDirect3DDevice9::LightEnable</b> method creates a light source represented by a <a href="/windows/desktop/direct3d9/d3dlight9">D3DLIGHT9</a> structure with the following properties and sets its enabled state to the value specified in bEnable.

<table>
<tr>
<th>Member</th>
<th>Default</th>
</tr>
<tr>
<td>Type
    
    </td>
<td>D3DLIGHT_DIRECTIONAL</td>
</tr>
<tr>
<td>Diffuse
    
    </td>
<td>(R:1, G:1, B:1, A:0)</td>
</tr>
<tr>
<td>Specular
    
    </td>
<td>(R:0, G:0, B:0, A:0)</td>
</tr>
<tr>
<td>Ambient
    
    </td>
<td>(R:0, G:0, B:0, A:0)</td>
</tr>
<tr>
<td>Position
    
    </td>
<td>(0, 0, 0)</td>
</tr>
<tr>
<td>Direction
    
    </td>
<td>(0, 0, 1)</td>
</tr>
<tr>
<td>Range
    
    </td>
<td>0</td>
</tr>
<tr>
<td>Falloff
    
    </td>
<td>0</td>
</tr>
<tr>
<td>Attenuation0
    
    </td>
<td>0</td>
</tr>
<tr>
<td>Attenuation1
    
    </td>
<td>0</td>
</tr>
<tr>
<td>Attenuation2
    
    </td>
<td>0</td>
</tr>
<tr>
<td>Theta
    
    </td>
<td>0</td>
</tr>
<tr>
<td>Phi
    
    </td>
<td>0</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight">IDirect3DDevice9::GetLight</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable">IDirect3DDevice9::GetLightEnable</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight">IDirect3DDevice9::SetLight</a>
