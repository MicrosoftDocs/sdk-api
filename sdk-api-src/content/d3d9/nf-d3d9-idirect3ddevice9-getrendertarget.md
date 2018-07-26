---
UID: NF:d3d9.IDirect3DDevice9.GetRenderTarget
title: IDirect3DDevice9::GetRenderTarget
author: windows-sdk-content
description: Retrieves a render-target surface.
old-location: direct3d9\idirect3ddevice9__getrendertarget.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getrendertarget.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetRenderTarget, GetRenderTarget method [Direct3D 9], GetRenderTarget method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetRenderTarget method, IDirect3DDevice9.GetRenderTarget, IDirect3DDevice9::GetRenderTarget, d3d9helper/IDirect3DDevice9::GetRenderTarget, direct3d9.idirect3ddevice9__getrendertarget, e842104c-7fc7-8278-14e9-2a36b37e033b
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
 - IDirect3DDevice9.GetRenderTarget
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetRenderTarget


## -description


Retrieves a render-target surface.


## -parameters




### -param RenderTargetIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Index of the render target. See Remarks.


### -param ppRenderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface, representing the returned render-target surface for this device. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL if one of the arguments is invalid, or D3DERR_NOTFOUND if there's no render target available for the given index.




## -remarks



Typically, methods that return state will not work on a device that is created using D3DCREATE_PUREDEVICE. This method however, will work even on a pure device because it returns an interface.

The device can now support multiple render targets. The number of render targets supported by a device is contained in the NumSimultaneousRTs member of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>. See <a href="https://msdn.microsoft.com/ae48c5ce-b7f5-4189-8b04-880836be3fe0">Multiple Render Targets (Direct3D 9)</a>.

Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using the <b>IDirect3DSurface9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/e194af98-492a-4650-acca-68ebe0cd759c">IDirect3DDevice9::SetRenderTarget</a>
 

 

