---
UID: NF:d3d9.IDirect3DDevice9.SetScissorRect
title: IDirect3DDevice9::SetScissorRect
author: windows-sdk-content
description: Sets the scissor rectangle.
old-location: direct3d9\idirect3ddevice9__setscissorrect.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setscissorrect.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetScissorRect method, IDirect3DDevice9.SetScissorRect, IDirect3DDevice9::SetScissorRect, SetScissorRect, SetScissorRect method [Direct3D 9], SetScissorRect method [Direct3D 9],IDirect3DDevice9 interface, c088567d-a486-1e7d-7863-886a85f0ecbb, d3d9helper/IDirect3DDevice9::SetScissorRect, direct3d9.idirect3ddevice9__setscissorrect
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
 - IDirect3DDevice9.SetScissorRect
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetScissorRect


## -description


Sets the scissor rectangle.


## -parameters




### -param pRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that defines the rendering area within the render target if scissor test is enabled. This parameter may not be <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -remarks



The scissor rectangle is used as a rectangular clipping region.

See <a href="https://msdn.microsoft.com/en-us/library/Bb147318(v=VS.85).aspx">Rectangles (Direct3D 9)</a> for further information on the use of rectangles in DirectX.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

