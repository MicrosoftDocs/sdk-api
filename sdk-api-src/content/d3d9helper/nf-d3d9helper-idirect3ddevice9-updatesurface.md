---
UID: NF:d3d9helper.IDirect3DDevice9.UpdateSurface
title: IDirect3DDevice9::UpdateSurface
author: windows-sdk-content
description: Copies rectangular subsets of pixels from one surface to another.
old-location: direct3d9\idirect3ddevice9__updatesurface.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__updatesurface.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],UpdateSurface method, IDirect3DDevice9.UpdateSurface, IDirect3DDevice9::UpdateSurface, UpdateSurface, UpdateSurface method [Direct3D 9], UpdateSurface method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::UpdateSurface, df5d6a49-ae43-30a0-f148-f2df8e51de81, direct3d9.idirect3ddevice9__updatesurface
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
 - IDirect3DDevice9.UpdateSurface
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::UpdateSurface


## -description


Copies rectangular subsets of pixels from one surface to another. 


## -parameters




### -param pSourceSurface [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface, representing the source surface. This parameter must point to a different surface than pDestinationSurface. 


### -param pSourceRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a rectangle on the source surface. Specifying <b>NULL</b> for this parameter causes the entire surface to be copied. 


### -param pDestinationSurface [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface, representing the destination surface.


### -param pDestPoint






#### - pDestinationPoint [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">POINT</a>*</b>

Pointer to the upper left corner of the destination rectangle. Specifying <b>NULL</b> for this parameter causes the entire surface to be copied. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL.




## -remarks



This method is similar to CopyRects in DirectX 8.

This function has the following restrictions.

<ul>
<li>The source surface must have been created with D3DPOOL_SYSTEMMEM.</li>
<li>The destination surface must have been created with D3DPOOL_DEFAULT.</li>
<li>Neither surface can be locked or holding an outstanding device context.</li>
<li>Neither surface can be created with multisampling. The only valid flag for both surfaces is D3DMULTISAMPLE_NONE.</li>
<li>The surface format cannot be a depth stencil format.</li>
<li>The source and dest rects must fit within the surface.</li>
<li>No stretching or shrinking is allowed (the rects must be the same size).</li>
<li>The source format must match the dest format.</li>
</ul>
The following table shows the supported combinations.

<table>
<tr>
<th></th>
<th></th>
<th>Dest formats</th>
<th></th>
<th></th>
<th></th>
</tr>
<tr>
<th></th>
<td></td>
<td>Texture</td>
<td>RT texture</td>
<td>RT</td>
<td>Off-screen plain</td>
</tr>
<tr>
<th>Src formats</th>
<td>Texture</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes*</td>
<td>Yes</td>
</tr>
<tr>
<th></th>
<td>RT texture</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th></th>
<td>RT</td>
<td>No</td>
<td>No</td>
<td>No</td>
<td>No</td>
</tr>
<tr>
<th></th>
<td>Off-screen plain</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
<td>Yes</td>
</tr>
</table>
 

* If the driver does not support the requested copy, it will be emulated using lock and copy.

If the application needs to copy data from a D3DPOOL_DEFAULT render target to a D3DPOOL_SYSTEMMEM surface, it can use <a href="https://msdn.microsoft.com/9fc6121c-3da8-49d8-9bd6-c8654ce90100">GetRenderTargetData</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

