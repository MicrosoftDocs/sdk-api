---
UID: NF:d3d9helper.IDirect3DDevice9.Present
title: IDirect3DDevice9::Present
author: windows-sdk-content
description: Presents the contents of the next buffer in the sequence of back buffers owned by the device.
old-location: direct3d9\idirect3ddevice9__present.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__present.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],Present method, IDirect3DDevice9.Present, IDirect3DDevice9::Present, Present, Present method [Direct3D 9], Present method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::Present, dec6b9d2-0577-093b-3855-599ed58adc87, direct3d9.idirect3ddevice9__present
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
 - IDirect3DDevice9.Present
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::Present


## -description


Presents the contents of the next buffer in the sequence of back buffers owned by the device.


## -parameters




### -param pSourceRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a value that must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. pSourceRect is a pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure containing the source rectangle. If <b>NULL</b>, the entire source surface is presented. If the rectangle exceeds the source surface, the rectangle is clipped to the source surface. 


### -param pDestRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a value that must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. pDestRect is a pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure containing the destination rectangle, in window client coordinates. If <b>NULL</b>, the entire client area is filled. If the rectangle exceeds the destination client area, the rectangle is clipped to the destination client area. 


### -param hDestWindowOverride [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Pointer to a destination window whose client area is taken as the target for this presentation. If this value is <b>NULL</b>, the runtime uses the <b>hDeviceWindow</b> member of <a href="https://msdn.microsoft.com/en-us/library/Bb172588(v=VS.85).aspx">D3DPRESENT_PARAMETERS</a> for the presentation.


### -param pDirtyRegion [in]

Type: <b>const <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>*</b>

Value must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. For more information about swap chains, see <a href="https://msdn.microsoft.com/en-us/library/Bb173393(v=VS.85).aspx">Flipping Surfaces (Direct3D 9)</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb172612(v=VS.85).aspx">D3DSWAPEFFECT</a>. If this value is non-<b>NULL</b>, the contained region is expressed in back buffer coordinates. The rectangles within the region are the minimal set of pixels that need to be updated. This method takes these rectangles into account when optimizing the presentation by copying only the pixels within the region, or some suitably expanded set of rectangles. This is an aid to optimization only, and the application should not rely on the region being copied exactly. The implementation can choose to copy the whole source rectangle. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Possible return values include: D3D_OK or D3DERR_DEVICEREMOVED (see <a href="https://msdn.microsoft.com/en-us/library/Bb172554(v=VS.85).aspx">D3DERR</a>).




## -remarks



If necessary, a stretch operation is applied to transfer the pixels within the source rectangle to the destination rectangle in the client area of the target window. 

<b>Present</b> will fail, returning D3DERR_INVALIDCALL, if called between BeginScene and EndScene pairs unless the render target is not the current render target (such as the back buffer you get from creating an additional swap chain). This is a new behavior for Direct3D 9. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174714(v=VS.85).aspx">Lost Devices (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb147217(v=VS.85).aspx">Multihead (Direct3D 9)</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174425(v=VS.85).aspx">Reset</a>
 

 

