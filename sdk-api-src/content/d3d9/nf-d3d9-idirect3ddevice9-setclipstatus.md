---
UID: NF:d3d9.IDirect3DDevice9.SetClipStatus
title: IDirect3DDevice9::SetClipStatus
author: windows-sdk-content
description: Sets the clip status.
old-location: direct3d9\idirect3ddevice9__setclipstatus.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setclipstatus.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 7c296c17-f98d-8458-efa7-95bbfde39651, IDirect3DDevice9 interface [Direct3D 9],SetClipStatus method, IDirect3DDevice9.SetClipStatus, IDirect3DDevice9::SetClipStatus, SetClipStatus, SetClipStatus method [Direct3D 9], SetClipStatus method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetClipStatus, direct3d9.idirect3ddevice9__setclipstatus
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
 - IDirect3DDevice9.SetClipStatus
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetClipStatus


## -description


Sets the clip status.


## -parameters




### -param pClipStatus [in]

Type: <b>const <a href="https://msdn.microsoft.com/3ea8631c-a967-4d24-a49a-1751b3ee6077">D3DCLIPSTATUS9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/3ea8631c-a967-4d24-a49a-1751b3ee6077">D3DCLIPSTATUS9</a> structure, describing the clip status settings to be set. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 If one of the arguments is invalid, the return value is D3DERR_INVALIDCALL.




## -remarks



Clip status is used during software vertex processing. Therefore, this method is not supported on pure or nonpure hardware processing devices. For more information about pure devices, see <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a>.

When clipping is enabled during vertex processing (by <a href="https://msdn.microsoft.com/0a34ecb6-6437-46dc-aa79-bf4d24395a86">IDirect3DDevice9::ProcessVertices</a>, <a href="https://msdn.microsoft.com/b83110ba-85af-4f02-b651-9e64c37269f5">IDirect3DDevice9::DrawPrimitive</a>, or other drawing functions), Direct3D computes a clip code for every vertex. The clip code is a combination of D3DCS_* bits. When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code. Direct3D maintains the clip status using <a href="https://msdn.microsoft.com/3ea8631c-a967-4d24-a49a-1751b3ee6077">D3DCLIPSTATUS9</a>, which has ClipUnion and ClipIntersection members. ClipUnion is a bitwise "OR" of all vertex clip codes and ClipIntersection is a bitwise "AND" of all vertex clip codes. Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection. When D3DRS_CLIPPING is set to <b>FALSE</b>, ClipUnion and ClipIntersection are set to zero. Direct3D updates the clip status during drawing calls. To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.

Clip status is not updated by <a href="https://msdn.microsoft.com/478b4a3d-3366-47ec-8a66-92aa2aa06477">IDirect3DDevice9::DrawRectPatch</a> and <a href="https://msdn.microsoft.com/9076fbe6-0f14-4b28-8f34-145e4eac6f22">IDirect3DDevice9::DrawTriPatch</a> because there is no software emulation for them.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/b8a68504-bc0f-4d36-a3f4-729fa9ab5004">IDirect3DDevice9::GetClipStatus</a>
 

 

