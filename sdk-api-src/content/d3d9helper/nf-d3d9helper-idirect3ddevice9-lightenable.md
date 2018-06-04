---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDirect3DDevice9::LightEnable


## -description


Enables or disables a set of lighting parameters within a device.


## -parameters




### -param Index




### -param Enable






#### - LightIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Zero-based index of the set of lighting parameters that are the target of this method. 


#### - bEnable [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value that indicates if the set of lighting parameters are being enabled or disabled. Set this parameter to <b>TRUE</b> to enable lighting with the parameters at the specified index, or <b>FALSE</b> to disable it. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



If a value for LightIndex is outside the range of the light property sets assigned within the device, the <b>IDirect3DDevice9::LightEnable</b> method creates a light source represented by a <a href="https://msdn.microsoft.com/25ce9d72-949c-41fc-8e3b-146d6a2de0dc">D3DLIGHT9</a> structure with the following properties and sets its enabled state to the value specified in bEnable.

<table>
<tr>
<th>Member</th>
<th>Default</th>
</tr>
<tr>
<td>
    
    Type
    
    </td>
<td>D3DLIGHT_DIRECTIONAL</td>
</tr>
<tr>
<td>
    
    Diffuse
    
    </td>
<td>(R:1, G:1, B:1, A:0)</td>
</tr>
<tr>
<td>
    
    Specular
    
    </td>
<td>(R:0, G:0, B:0, A:0)</td>
</tr>
<tr>
<td>
    
    Ambient
    
    </td>
<td>(R:0, G:0, B:0, A:0)</td>
</tr>
<tr>
<td>
    
    Position
    
    </td>
<td>(0, 0, 0)</td>
</tr>
<tr>
<td>
    
    Direction
    
    </td>
<td>(0, 0, 1)</td>
</tr>
<tr>
<td>
    
    Range
    
    </td>
<td>0</td>
</tr>
<tr>
<td>
    
    Falloff
    
    </td>
<td>0</td>
</tr>
<tr>
<td>
    
    Attenuation0
    
    </td>
<td>0</td>
</tr>
<tr>
<td>
    
    Attenuation1
    
    </td>
<td>0</td>
</tr>
<tr>
<td>
    
    Attenuation2
    
    </td>
<td>0</td>
</tr>
<tr>
<td>
    
    Theta
    
    </td>
<td>0</td>
</tr>
<tr>
<td>
    
    Phi
    
    </td>
<td>0</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/1e52be8e-7e24-400d-89c5-93dd316534bc">IDirect3DDevice9::GetLight</a>



<a href="https://msdn.microsoft.com/7dacc010-fef7-4fcb-8e3e-08b683476eef">IDirect3DDevice9::GetLightEnable</a>



<a href="https://msdn.microsoft.com/e1f07ba6-8a9f-4bac-8dad-16160559fa4c">IDirect3DDevice9::SetLight</a>
 

 

