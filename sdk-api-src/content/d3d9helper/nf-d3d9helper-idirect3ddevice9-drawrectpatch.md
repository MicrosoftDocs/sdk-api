---
UID: NF:d3d9helper.IDirect3DDevice9.DrawRectPatch
title: IDirect3DDevice9::DrawRectPatch
author: windows-sdk-content
description: Draws a rectangular patch using the currently set streams.
old-location: direct3d9\idirect3ddevice9__drawrectpatch.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__drawrectpatch.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 9f04b48b-012e-3487-432e-10ce6b33782a, DrawRectPatch, DrawRectPatch method [Direct3D 9], DrawRectPatch method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],DrawRectPatch method, IDirect3DDevice9.DrawRectPatch, IDirect3DDevice9::DrawRectPatch, d3d9helper/IDirect3DDevice9::DrawRectPatch, direct3d9.idirect3ddevice9__drawrectpatch
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.DrawRectPatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::DrawRectPatch


## -description


Draws a rectangular patch using the currently set streams.


## -parameters




### -param Handle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Handle to the rectangular patch to draw. 


### -param pNumSegs [in]

Type: <b>const float*</b>

Pointer to an array of four floating-point values that identify the number of segments each edge of the rectangle patch should be divided into when tessellated. See <a href="https://msdn.microsoft.com/5f195009-d047-4dc0-a386-e1a434914e34">D3DRECTPATCH_INFO</a>. 


### -param pRectPatchInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/5f195009-d047-4dc0-a386-e1a434914e34">D3DRECTPATCH_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/5f195009-d047-4dc0-a386-e1a434914e34">D3DRECTPATCH_INFO</a> structure, describing the rectangular patch to draw. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.




## -remarks



For static patches: Set the vertex shader, set the appropriate streams, supply patch information in the pRectPatchInfo parameter, and specify a handle so that Direct3D can capture and cache information. Call <b>IDirect3DDevice9::DrawRectPatch</b> subsequently with pRectPatchInfo set to <b>NULL</b> to efficiently draw the patch. When drawing a cached patch, the currently set streams are ignored. Override the cached pNumSegs by specifying a new value for pNumSegs. When rendering a cached patch, you must set the same vertex shader that was set when it was captured.

Calling <b>IDirect3DDevice9::DrawRectPatch</b> with a handle invalidates the same handle cached by a previous <a href="https://msdn.microsoft.com/9076fbe6-0f14-4b28-8f34-145e4eac6f22">IDirect3DDevice9::DrawTriPatch</a> call.

For dynamic patches, the patch data changes for every rendering of the patch, so it is not efficient to cache information. The application can convey this to Direct3D by setting Handle to 0. In this case, Direct3D draws the patch using the currently set streams and the pNumSegs values, and does not cache any information. It is not valid to simultaneously set Handle to 0 and pRectPatchInfo to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/2febb03e-63ed-4c16-b6ba-1927f749c1ca">IDirect3DDevice9::DeletePatch</a>



<a href="https://msdn.microsoft.com/7aa4f3ab-cfce-4f8f-a538-384f038fd324">Using Higher-Order Primitives (Direct3D 9)</a>
 

 

