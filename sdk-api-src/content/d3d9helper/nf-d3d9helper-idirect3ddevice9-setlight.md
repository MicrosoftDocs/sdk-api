---
UID: NF:d3d9helper.IDirect3DDevice9.SetLight
title: IDirect3DDevice9::SetLight (d3d9helper.h)
description: The IDirect3DDevice9::SetLight method (d3d9helper.h) assigns a set of lighting properties for this device.
helpviewer_keywords: ["01be5e3b-cd10-6899-0e92-5f0874741380","IDirect3DDevice9 interface [Direct3D 9]","SetLight method","IDirect3DDevice9.SetLight","IDirect3DDevice9::SetLight","SetLight","SetLight method [Direct3D 9]","SetLight method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetLight","direct3d9.idirect3ddevice9__setlight"]
old-location: direct3d9\idirect3ddevice9__setlight.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setlight.htm
ms.date: 08/11/2022
ms.keywords: 01be5e3b-cd10-6899-0e92-5f0874741380, IDirect3DDevice9 interface [Direct3D 9],SetLight method, IDirect3DDevice9.SetLight, IDirect3DDevice9::SetLight, SetLight, SetLight method [Direct3D 9], SetLight method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetLight, direct3d9.idirect3ddevice9__setlight
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
 - IDirect3DDevice9::SetLight
 - d3d9helper/IDirect3DDevice9::SetLight
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
 - IDirect3DDevice9.SetLight
---

# IDirect3DDevice9::SetLight


## -description

Assigns a set of lighting properties for this device.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Zero-based index of the set of lighting properties to set. If a set of lighting properties exists at this index, it is overwritten by the new properties specified in pLight.

### -param unnamedParam2 [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dlight9">D3DLIGHT9</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dlight9">D3DLIGHT9</a> structure, containing the lighting parameters to set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

Set light properties by preparing a <a href="/windows/desktop/direct3d9/d3dlight9">D3DLIGHT9</a> structure and then calling the <b>IDirect3DDevice9::SetLight</b> method. The <b>IDirect3DDevice9::SetLight</b> method accepts the index at which the device should place the set of light properties to its internal list of light properties, and the address of a prepared <b>D3DLIGHT9</b> structure that defines those properties. You can call <b>IDirect3DDevice9::SetLight</b> with new information as needed to update the light's illumination properties.

The system allocates memory to accommodate a set of lighting properties each time you call the <b>IDirect3DDevice9::SetLight</b> method with an index that has never been assigned properties. Applications can set a number of lights, with only a subset of the assigned lights enabled at a time. Check the MaxActiveLights member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure when you retrieve device capabilities to determine the maximum number of active lights supported by that device. If you no longer need a light, you can disable it or overwrite it with a new set of light properties.

The following example prepares and sets properties for a white point-light whose emitted light will not attenuate over distance.


```

// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface.
D3DLIGHT9 d3dLight;
HRESULT   hr;
    
// Initialize the structure.
ZeroMemory(&d3dLight, sizeof(d3dLight));
    
// Set up a white point light.
d3dLight.Type = D3DLIGHT_POINT;
d3dLight.Diffuse.r  = 1.0f;
d3dLight.Diffuse.g  = 1.0f;
d3dLight.Diffuse.b  = 1.0f;
d3dLight.Ambient.r  = 1.0f;
d3dLight.Ambient.g  = 1.0f;
d3dLight.Ambient.b  = 1.0f;
d3dLight.Specular.r = 1.0f;
d3dLight.Specular.g = 1.0f;
d3dLight.Specular.b = 1.0f;
    
// Position it high in the scene and behind the user.
// Remember, these coordinates are in world space, so
// the user could be anywhere in world space, too. 
// For the purposes of this example, assume the user
// is at the origin of world space.
d3dLight.Position.x = 0.0f;
d3dLight.Position.y = 1000.0f;
d3dLight.Position.z = -100.0f;
    
// Don't attenuate.
d3dLight.Attenuation0 = 1.0f; 
d3dLight.Range        = 1000.0f;
    
// Set the property information for the first light.
hr = d3dDevice->SetLight(0, &d3dLight);
if (SUCCEEDED(hr))
    // Handle Success
else
    // Handle failure

```


Enable a light source by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">IDirect3DDevice9::LightEnable</a> method for the device.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight">IDirect3DDevice9::GetLight</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable">IDirect3DDevice9::GetLightEnable</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">IDirect3DDevice9::LightEnable</a>
