---
UID: NF:d3d9.IDirect3DSwapChain9.GetFrontBufferData
title: IDirect3DSwapChain9::GetFrontBufferData
author: windows-sdk-content
description: Generates a copy of the swapchain's front buffer and places that copy in a system memory buffer provided by the application.
old-location: direct3d9\idirect3dswapchain9__getfrontbufferdata.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9__getfrontbufferdata.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 8f442969-657a-a5ab-1aa3-ff227fe2f705, GetFrontBufferData, GetFrontBufferData method [Direct3D 9], GetFrontBufferData method [Direct3D 9],IDirect3DSwapChain9 interface, IDirect3DSwapChain9 interface [Direct3D 9],GetFrontBufferData method, IDirect3DSwapChain9.GetFrontBufferData, IDirect3DSwapChain9::GetFrontBufferData, d3d9helper/IDirect3DSwapChain9::GetFrontBufferData, direct3d9.idirect3dswapchain9__getfrontbufferdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
req.redist: 
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
 - IDirect3DSwapChain9.GetFrontBufferData
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DSwapChain9::GetFrontBufferData


## -description


Generates a copy of the swapchain's front buffer and places that copy in a system memory buffer provided by the application.


## -parameters




### -param pDestSurface [in, out]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface that will receive a copy of the swapchain's front buffer. The data is returned in successive rows with no intervening space, starting from the vertically highest row to the lowest.  For windowed mode, the size of the destination surface should be the size of the desktop. For full screen mode, the size of the destination surface should be the screen size. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 If BackBuffer exceeds or equals the total number of back buffers, the function fails and returns D3DERR_INVALIDCALL. 




## -remarks



Calling this method will increase the internal reference count on the <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface. Failure to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when finished using this <b>IDirect3DSurface9</b> interface results in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>
 

 

