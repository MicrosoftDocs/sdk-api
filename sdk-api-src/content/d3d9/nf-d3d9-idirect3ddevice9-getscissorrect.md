---
UID: NF:d3d9.IDirect3DDevice9.GetScissorRect
title: IDirect3DDevice9::GetScissorRect
author: windows-sdk-content
description: Gets the scissor rectangle.
old-location: direct3d9\idirect3ddevice9__getscissorrect.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getscissorrect.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: 7de78b9b-0918-15ce-f2b5-f1b433033d52, GetScissorRect, GetScissorRect method [Direct3D 9], GetScissorRect method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetScissorRect method, IDirect3DDevice9.GetScissorRect, IDirect3DDevice9::GetScissorRect, d3d9helper/IDirect3DDevice9::GetScissorRect, direct3d9.idirect3ddevice9__getscissorrect
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
 - IDirect3DDevice9.GetScissorRect
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetScissorRect


## -description


Gets the scissor rectangle.


## -parameters




### -param pRect [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Returns a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that defines the rendering area within the render target if scissor test is enabled.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.




## -remarks



The scissor rectangle is used as a rectangular clipping region.

See <a href="https://msdn.microsoft.com/9e271652-1673-42ea-b1f4-31ac63c397c5">Rectangles (Direct3D 9)</a> for further information on the use of rectangles in DirectX.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

