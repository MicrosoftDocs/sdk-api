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

# IDirect3DDevice9::DrawTriPatch


## -description


Draws a triangular patch using the currently set streams.


## -parameters




### -param Handle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Handle to the triangular patch to draw. 


### -param pNumSegs [in]

Type: <b>const float*</b>

Pointer to an array of three floating-point values that identify the number of segments each edge of the triangle patch should be divided into when tessellated. See <a href="https://msdn.microsoft.com/3f97120b-3b32-4f95-8614-7b263ff330db">D3DTRIPATCH_INFO</a>. 


### -param pTriPatchInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/3f97120b-3b32-4f95-8614-7b263ff330db">D3DTRIPATCH_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/3f97120b-3b32-4f95-8614-7b263ff330db">D3DTRIPATCH_INFO</a> structure, describing the triangular high-order patch to draw. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be 
     D3DERR_INVALIDCALL.




## -remarks



For static patches: Set the vertex shader, set the appropriate streams, supply patch information in the pTriPatchInfo parameter, and specify a handle so that Direct3D can capture and cache information. To efficiently draw the patch, call <b>IDirect3DDevice9::DrawTriPatch</b> with pTriPatchInfo set to <b>NULL</b>. When drawing a cached patch, the currently set streams are ignored. Override the cached pNumSegs by specifying a new value for pNumSegs. When rendering a cached patch, you must set the same vertex shader that was set when it was captured.

Calling <b>IDirect3DDevice9::DrawTriPatch</b> with a handle invalidates the same handle cached by a previous <a href="https://msdn.microsoft.com/478b4a3d-3366-47ec-8a66-92aa2aa06477">IDirect3DDevice9::DrawRectPatch</a> call.

For dynamic patches, the patch data changes for every rendering of the patch so it is not efficient to cache information. The application can convey this to Direct3D by setting Handle to 0. In this case, Direct3D draws the patch using the currently set streams and the pNumSegs values, and does not cache any information. It is not valid to simultaneously set Handle to 0 and pTriPatchInfo to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/7aa4f3ab-cfce-4f8f-a538-384f038fd324">Using Higher-Order Primitives (Direct3D 9)</a>
 

 

