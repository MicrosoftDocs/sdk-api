---
UID: NF:d3d9.IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx
title: IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx
author: windows-sdk-content
description: Create an off-screen surface.
old-location: direct3d9\idirect3ddevice9ex_createoffscreenplainsurfaceex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_createoffscreenplainsurfaceex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 63d121fa-1b4f-16db-b792-c30558006ddb, CreateOffscreenPlainSurfaceEx, CreateOffscreenPlainSurfaceEx method [Direct3D 9], CreateOffscreenPlainSurfaceEx method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CreateOffscreenPlainSurfaceEx method, IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx, IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx, d3d9/IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx, direct3d9.idirect3ddevice9ex_createoffscreenplainsurfaceex
ms.topic: method
req.header: d3d9.h
req.include-header: 
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
 - IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx


## -description


Create an off-screen surface.


## -parameters




### -param Width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the surface.


### -param Height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the surface.


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a></b>

Format of the surface. See <a href="https://msdn.microsoft.com/en-us/library/Bb172558(v=VS.85).aspx">D3DFORMAT</a>. 


### -param Pool [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a></b>

Surface pool type. See <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a>.


### -param ppSurface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>**</b>

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>  interface created.


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/en-us/library/Bb219800(v=VS.85).aspx">share resources</a>.


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more <a href="https://msdn.microsoft.com/en-us/library/Bb172625(v=VS.85).aspx">D3DUSAGE</a> constants which can be OR'd together. Value of 0 indicates no usage.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.




## -remarks



D3DPOOL_SCRATCH will return a surface that has identical characteristics to a surface created by the DirectX 8.x method CreateImageSurface.

D3DPOOL_DEFAULT is the appropriate pool for use with the <a href="https://msdn.microsoft.com/en-us/library/Bb174471(v=VS.85).aspx">IDirect3DDevice9::StretchRect</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb174353(v=VS.85).aspx">IDirect3DDevice9::ColorFill</a>.

D3DPOOL_MANAGED is not allowed when creating an offscreen plain surface. For more information about memory pools, see <a href="https://msdn.microsoft.com/en-us/library/Bb172584(v=VS.85).aspx">D3DPOOL</a>.

Off-screen plain surfaces are always lockable, regardless of their pool types.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>
 

 

