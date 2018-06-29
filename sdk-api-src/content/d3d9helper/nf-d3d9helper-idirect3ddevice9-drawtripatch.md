---
UID: NF:d3d9helper.IDirect3DDevice9.DrawTriPatch
title: IDirect3DDevice9::DrawTriPatch
author: windows-sdk-content
description: Draws a triangular patch using the currently set streams.
old-location: direct3d9\idirect3ddevice9__drawtripatch.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawtripatch.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 4db7630f-e9d1-c5ec-df98-7a2f4cde37cc, DrawTriPatch, DrawTriPatch method [Direct3D 9], DrawTriPatch method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawTriPatch method, IDirect3DDevice9.DrawTriPatch, IDirect3DDevice9::DrawTriPatch, d3d9helper/IDirect3DDevice9::DrawTriPatch, direct3d9.idirect3ddevice9__drawtripatch
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
 - IDirect3DDevice9.DrawTriPatch
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::DrawTriPatch


## -description


Draws a triangular patch using the currently set streams.


## -parameters




### -param Handle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Handle to the triangular patch to draw. 


### -param pNumSegs [in]

Type: <b>const float*</b>

Pointer to an array of three floating-point values that identify the number of segments each edge of the triangle patch should be divided into when tessellated. See <a href="https://msdn.microsoft.com/library/Bb172620(v=VS.85).aspx">D3DTRIPATCH_INFO</a>. 


### -param pTriPatchInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Bb172620(v=VS.85).aspx">D3DTRIPATCH_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/Bb172620(v=VS.85).aspx">D3DTRIPATCH_INFO</a> structure, describing the triangular high-order patch to draw. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.




## -remarks



For static patches: Set the vertex shader, set the appropriate streams, supply patch information in the pTriPatchInfo parameter, and specify a handle so that Direct3D can capture and cache information. To efficiently draw the patch, call <b>IDirect3DDevice9::DrawTriPatch</b> with pTriPatchInfo set to <b>NULL</b>. When drawing a cached patch, the currently set streams are ignored. Override the cached pNumSegs by specifying a new value for pNumSegs. When rendering a cached patch, you must set the same vertex shader that was set when it was captured.

Calling <b>IDirect3DDevice9::DrawTriPatch</b> with a handle invalidates the same handle cached by a previous <a href="https://msdn.microsoft.com/library/Bb174373(v=VS.85).aspx">IDirect3DDevice9::DrawRectPatch</a> call.

For dynamic patches, the patch data changes for every rendering of the patch so it is not efficient to cache information. The application can convey this to Direct3D by setting Handle to 0. In this case, Direct3D draws the patch using the currently set streams and the pNumSegs values, and does not cache any information. It is not valid to simultaneously set Handle to 0 and pTriPatchInfo to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/library/Bb206314(v=VS.85).aspx">Using Higher-Order Primitives (Direct3D 9)</a>
 

 

