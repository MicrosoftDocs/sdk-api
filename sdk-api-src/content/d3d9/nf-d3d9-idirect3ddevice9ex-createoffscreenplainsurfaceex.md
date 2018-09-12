---
UID: NF:d3d9.IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx
title: IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx
author: windows-sdk-content
description: Create an off-screen surface.
old-location: direct3d9\idirect3ddevice9ex_createoffscreenplainsurfaceex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_createoffscreenplainsurfaceex.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 63d121fa-1b4f-16db-b792-c30558006ddb, CreateOffscreenPlainSurfaceEx, CreateOffscreenPlainSurfaceEx method [Direct3D 9], CreateOffscreenPlainSurfaceEx method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],CreateOffscreenPlainSurfaceEx method, IDirect3DDevice9Ex.CreateOffscreenPlainSurfaceEx, IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx, d3d9/IDirect3DDevice9Ex::CreateOffscreenPlainSurfaceEx, direct3d9.idirect3ddevice9ex_createoffscreenplainsurfaceex
ms.prod: windows-hardware
ms.technology: windows-devices
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

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Format of the surface. See <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>. 


### -param Pool [in]

Type: <b><a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a></b>

Surface pool type. See <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a>.


### -param ppSurface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>**</b>

Pointer to the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>  interface created.


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">share resources</a>.


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a> constants which can be OR'd together. Value of 0 indicates no usage.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be the following:
     D3DERR_INVALIDCALL.




## -remarks



D3DPOOL_SCRATCH will return a surface that has identical characteristics to a surface created by the DirectX 8.x method CreateImageSurface.

D3DPOOL_DEFAULT is the appropriate pool for use with the <a href="https://msdn.microsoft.com/1ad6d48f-8420-461a-96b5-e730ac06c393">IDirect3DDevice9::StretchRect</a> and <a href="https://msdn.microsoft.com/de8c1f15-cb82-4c20-86e0-78b730dae55d">IDirect3DDevice9::ColorFill</a>.

D3DPOOL_MANAGED is not allowed when creating an offscreen plain surface. For more information about memory pools, see <a href="https://msdn.microsoft.com/29720b5f-16d7-4bd9-a7bd-e4dbfb00070b">D3DPOOL</a>.

Off-screen plain surfaces are always lockable, regardless of their pool types.




## -see-also




<a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>
 

 

