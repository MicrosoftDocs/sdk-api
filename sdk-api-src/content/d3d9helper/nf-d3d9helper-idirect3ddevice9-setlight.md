---
UID: NF:d3d9helper.IDirect3DDevice9.SetLight
title: IDirect3DDevice9::SetLight
author: windows-sdk-content
description: Assigns a set of lighting properties for this device.
old-location: direct3d9\idirect3ddevice9__setlight.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setlight.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 01be5e3b-cd10-6899-0e92-5f0874741380, IDirect3DDevice9 interface [Direct3D 9],SetLight method, IDirect3DDevice9.SetLight, IDirect3DDevice9::SetLight, SetLight, SetLight method [Direct3D 9], SetLight method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetLight, direct3d9.idirect3ddevice9__setlight
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
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
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetLight


## -description


Assigns a set of lighting properties for this device.


## -parameters




### -param Index [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Zero-based index of the set of lighting properties to set. If a set of lighting properties exists at this index, it is overwritten by the new properties specified in pLight. 


### -param D3DLIGHT9






#### - pLight [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb172566(v=VS.85).aspx">D3DLIGHT9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172566(v=VS.85).aspx">D3DLIGHT9</a> structure, containing the lighting parameters to set. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Set light properties by preparing a <a href="https://msdn.microsoft.com/en-us/library/Bb172566(v=VS.85).aspx">D3DLIGHT9</a> structure and then calling the <b>IDirect3DDevice9::SetLight</b> method. The 
    
    <b>IDirect3DDevice9::SetLight</b> method accepts the index at which the device should place the set of light properties to its internal list of light properties, and the address of a prepared <b>D3DLIGHT9</b> structure that defines those properties. You can call <b>IDirect3DDevice9::SetLight</b> with new information as needed to update the light's illumination properties.

The system allocates memory to accommodate a set of lighting properties each time you call the <b>IDirect3DDevice9::SetLight</b> method with an index that has never been assigned properties. Applications can set a number of lights, with only a subset of the assigned lights enabled at a time. Check the MaxActiveLights member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> structure when you retrieve device capabilities to determine the maximum number of active lights supported by that device. If you no longer need a light, you can disable it or overwrite it with a new set of light properties.

The following example prepares and sets properties for a white point-light whose emitted light will not attenuate over distance.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface.
D3DLIGHT9 d3dLight;
HRESULT   hr;
    
// Initialize the structure.
ZeroMemory(&amp;d3dLight, sizeof(d3dLight));
    
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
hr = d3dDevice-&gt;SetLight(0, &amp;d3dLight);
if (SUCCEEDED(hr))
    // Handle Success
else
    // Handle failure
</pre>
</td>
</tr>
</table></span></div>
Enable a light source by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb174421(v=VS.85).aspx">IDirect3DDevice9::LightEnable</a> method for the device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174392(v=VS.85).aspx">IDirect3DDevice9::GetLight</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174393(v=VS.85).aspx">IDirect3DDevice9::GetLightEnable</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174421(v=VS.85).aspx">IDirect3DDevice9::LightEnable</a>
 

 

