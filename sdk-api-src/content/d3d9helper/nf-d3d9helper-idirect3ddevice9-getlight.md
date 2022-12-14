---
UID: NF:d3d9helper.IDirect3DDevice9.GetLight
title: IDirect3DDevice9::GetLight (d3d9helper.h)
description: The IDirect3DDevice9::GetLight method (d3d9.h) retrieves a set of lighting properties that this device uses.
helpviewer_keywords: ["63c42786-98b1-2b46-00cc-ad05ab2594f4","GetLight","GetLight method [Direct3D 9]","GetLight method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetLight method","IDirect3DDevice9.GetLight","IDirect3DDevice9::GetLight","d3d9helper/IDirect3DDevice9::GetLight","direct3d9.idirect3ddevice9__getlight"]
old-location: direct3d9\idirect3ddevice9__getlight.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getlight.htm
ms.date: 08/11/2022
ms.keywords: 63c42786-98b1-2b46-00cc-ad05ab2594f4, GetLight, GetLight method [Direct3D 9], GetLight method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetLight method, IDirect3DDevice9.GetLight, IDirect3DDevice9::GetLight, d3d9helper/IDirect3DDevice9::GetLight, direct3d9.idirect3ddevice9__getlight
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
 - IDirect3DDevice9::GetLight
 - d3d9helper/IDirect3DDevice9::GetLight
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
 - IDirect3DDevice9.GetLight
---

# IDirect3DDevice9::GetLight


## -description

Retrieves a set of lighting properties that this device uses.

## -parameters

### -param Index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Zero-based index of the lighting property set to retrieve. This method will fail if a lighting property has not been set for this index by calling the <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight">IDirect3DDevice9::SetLight</a> method.

### -param unnamedParam2 [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dlight9">D3DLight9</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dlight9">D3DLIGHT9</a> structure that is filled with the retrieved lighting-parameter set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other values in <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>.

Retrieve all the properties for an existing light source by calling the <b>IDirect3DDevice9::GetLight</b> method for the device. When calling the <b>IDirect3DDevice9::GetLight</b> method, pass the zero-based index of the light source for which the properties will be retrieved as the first parameter, and supply the address of a <a href="/windows/desktop/direct3d9/d3dlight9">D3DLIGHT9</a> structure as the second parameter. The device fills the <b>D3DLIGHT9</b> structure to describe the lighting properties it uses for the light source at that index.


```

// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DLight9 light;
    
// Get the property information for the first light.
hr = pd3dDevice->GetLight(0, &light);
if (SUCCEEDED(hr))
    // Handle Success
else
    // Handle failure

```


If you supply an index outside the range of the light sources assigned in the device, the <b>IDirect3DDevice9::GetLight</b> method fails, returning D3DERR_INVALIDCALL.

When you assign a set of light properties for a light source in a scene, the light source can be activated by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">IDirect3DDevice9::LightEnable</a> method for the device. New light sources are disabled by default. The <b>IDirect3DDevice9::LightEnable</b> method accepts two parameters. Set the first parameter to the zero-based index of the light source to be affected by the method, and set the second parameter to <b>TRUE</b> to enable the light or <b>FALSE</b> to disable it. The following code example illustrates the use of this method by enabling the first light source in the device's list of light source properties.


```

// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
    
hr = pd3dDevice->LightEnable(0, TRUE);
if (SUCCEEDED(hr))
    // Handle Success
else
    // Handle failure

```


Check the MaxActiveLights member of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure when you retrieve device capabilities to determine the maximum number of active lights supported by that device.

If you enable or disable a light that has no properties that are set with <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight">IDirect3DDevice9::SetLight</a>, the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">IDirect3DDevice9::LightEnable</a> method creates a light source with the properties listed in following table and enables or disables it.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable">IDirect3DDevice9::GetLightEnable</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">IDirect3DDevice9::LightEnable</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight">IDirect3DDevice9::SetLight</a>
