---
UID: NF:d3d9helper.IDirect3DDevice9.MultiplyTransform
title: IDirect3DDevice9::MultiplyTransform
author: windows-sdk-content
description: Multiplies a device's world, view, or projection matrices by a specified matrix.
old-location: direct3d9\idirect3ddevice9__multiplytransform.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__multiplytransform.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],MultiplyTransform method, IDirect3DDevice9.MultiplyTransform, IDirect3DDevice9::MultiplyTransform, MultiplyTransform, MultiplyTransform method [Direct3D 9], MultiplyTransform method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::MultiplyTransform, direct3d9.idirect3ddevice9__multiplytransform, fe383422-a888-e230-bf89-3ae4af8e8e7d
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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

Type: <b><a href="https://msdn.microsoft.com/library/Bb172619(v=VS.85).aspx">D3DTRANSFORMSTATETYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/library/Bb172619(v=VS.85).aspx">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="https://msdn.microsoft.com/library/Bb172623(v=VS.85).aspx">D3DTS_WORLDMATRIX</a> macro that identifies which device matrix is to be modified. The most common setting, <b>D3DTS_WORLDMATRIX</b>(0), modifies the world matrix, but you can specify that the method modify the view or projection matrices, if needed. 


#### - pMatrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Bb172573(v=VS.85).aspx">D3DMATRIX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/Bb172573(v=VS.85).aspx">D3DMATRIX</a> structure that modifies the current transformation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

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




<a href="https://msdn.microsoft.com/library/Bb172622(v=VS.85).aspx">D3DTS_WORLD</a>



<a href="https://msdn.microsoft.com/library/Bb172623(v=VS.85).aspx">D3DTS_WORLDMATRIX</a>



<a href="https://msdn.microsoft.com/library/Bb172624(v=VS.85).aspx">D3DTS_WORLDn</a>



<a href="https://msdn.microsoft.com/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/library/Bb174371(v=VS.85).aspx">IDirect3DDevice9::DrawPrimitive</a>



<a href="https://msdn.microsoft.com/library/Bb174463(v=VS.85).aspx">IDirect3DDevice9::SetTransform</a>
 

 

