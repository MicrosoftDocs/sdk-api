---
UID: NF:d3d9.IDirect3DDevice9.MultiplyTransform
title: IDirect3DDevice9::MultiplyTransform
author: windows-sdk-content
description: Multiplies a device's world, view, or projection matrices by a specified matrix.
old-location: direct3d9\idirect3ddevice9__multiplytransform.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__multiplytransform.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],MultiplyTransform method, IDirect3DDevice9.MultiplyTransform, IDirect3DDevice9::MultiplyTransform, MultiplyTransform, MultiplyTransform method [Direct3D 9], MultiplyTransform method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::MultiplyTransform, direct3d9.idirect3ddevice9__multiplytransform, fe383422-a888-e230-bf89-3ae4af8e8e7d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.MultiplyTransform
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::MultiplyTransform


## -description


Multiplies a device's world, view, or projection matrices by a specified matrix. 


## -parameters




### -param param




### -param D3DMATRIX






#### - State [in]

Type: <b><a href="https://msdn.microsoft.com/53535d9f-246a-42cf-82a2-fb3cf6d4ebac">D3DTRANSFORMSTATETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/53535d9f-246a-42cf-82a2-fb3cf6d4ebac">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a> macro that identifies which device matrix is to be modified. The most common setting, <b>D3DTS_WORLDMATRIX</b>(0), modifies the world matrix, but you can specify that the method modify the view or projection matrices, if needed. 


#### - pMatrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/d6b98a32-e745-4724-b8ce-a81a3f5416f3">D3DMATRIX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d6b98a32-e745-4724-b8ce-a81a3f5416f3">D3DMATRIX</a> structure that modifies the current transformation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if one of the arguments is invalid.




## -remarks



The multiplication order is pMatrix times State.

An application might use the <b>IDirect3DDevice9::MultiplyTransform</b> method to work with hierarchies of transformations. For example, the geometry and transformations describing an arm might be arranged in the following hierarchy.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    
    shoulder_transformation
    
    upper_arm geometry
    
    elbow transformation
    
    lower_arm geometry
    
    wrist transformation
    
    hand geometry
</pre>
</td>
</tr>
</table></span></div>
An application might use the following series of calls to render this hierarchy. Not all the parameters are shown in this pseudocode.
    
            

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDirect3DDevice9::SetTransform(D3DTS_WORLDMATRIX(0), 
                               shoulder_transform)
IDirect3DDevice9::DrawPrimitive(upper_arm)
IDirect3DDevice9::MultiplyTransform(D3DTS_WORLDMATRIX(0), 
                                    elbow_transform)
IDirect3DDevice9::DrawPrimitive(lower_arm)
IDirect3DDevice9::MultiplyTransform(D3DTS_WORLDMATRIX(0), 
                                    wrist_transform)
IDirect3DDevice9::DrawPrimitive(hand)</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2bf7ac8a-43d8-460e-a400-3b33e96441db">D3DTS_WORLD</a>



<a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a>



<a href="https://msdn.microsoft.com/cab444c2-b245-4d1a-a90c-745c92a2ea89">D3DTS_WORLDn</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/1dc94280-131f-47e8-8dd7-cea43dc6e6da">IDirect3DDevice9::SetTransform</a>
 

 

