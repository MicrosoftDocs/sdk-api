---
UID: NF:d3d9.IDirect3DDevice9.GetFrontBufferData
title: IDirect3DDevice9::GetFrontBufferData
author: windows-sdk-content
description: Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application.
old-location: direct3d9\idirect3ddevice9__getfrontbufferdata.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getfrontbufferdata.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetFrontBufferData, GetFrontBufferData method [Direct3D 9], GetFrontBufferData method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetFrontBufferData method, IDirect3DDevice9.GetFrontBufferData, IDirect3DDevice9::GetFrontBufferData, b122af3c-c0ea-2cbb-1c39-139ab45eff11, d3d9helper/IDirect3DDevice9::GetFrontBufferData, direct3d9.idirect3ddevice9__getfrontbufferdata
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
 - IDirect3DDevice9.GetFrontBufferData
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetFrontBufferData


## -description


Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application. 


## -parameters




### -param iSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An unsigned integer specifying the swap chain.


### -param pDestSurface [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface that will receive a copy of the contents of the front buffer. The data is returned in successive rows with no intervening space, starting from the vertically highest row on the device's output to the lowest.



For windowed mode, the size of the destination surface should be the size of the desktop. For full-screen mode, the size of the destination surface should be the screen size.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_DRIVERINTERNALERROR, D3DERR_DEVICELOST, D3DERR_INVALIDCALL




## -remarks



The buffer pointed to by pDestSurface will be filled with a representation of the front buffer, converted to the standard 32 bits per pixel format D3DFMT_A8R8G8B8. 

This method is the only way to capture an antialiased screen shot.

This function is very slow, by design, and should not be used in any performance-critical path.

For more information, see <a href="https://msdn.microsoft.com/dc4326ba-2ebc-4bca-8fba-02d8db739b8f">Lost Devices and Retrieved Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

