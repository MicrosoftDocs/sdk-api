---
UID: NF:d3d9.IDirect3DSurface9.ReleaseDC
title: IDirect3DSurface9::ReleaseDC
author: windows-sdk-content
description: Release a device context handle.
old-location: direct3d9\idirect3dsurface9__releasedc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__releasedc.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IDirect3DSurface9 interface [Direct3D 9],ReleaseDC method, IDirect3DSurface9.ReleaseDC, IDirect3DSurface9::ReleaseDC, ReleaseDC, ReleaseDC method [Direct3D 9], ReleaseDC method [Direct3D 9],IDirect3DSurface9 interface, c9032355-5437-491b-97b3-727d5c94fbfa, d3d9helper/IDirect3DSurface9::ReleaseDC, direct3d9.idirect3dsurface9__releasedc
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
 - IDirect3DSurface9.ReleaseDC
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DSurface9::ReleaseDC


## -description


Release a device context handle.


## -parameters




### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

Handle to a device context.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -remarks



An hdc is a Windows resource. It must be released after use so Windows can return it to the pool of available resources.

This method will release only the device context returned by <a href="https://msdn.microsoft.com/3456470b-60c5-4ac2-bb71-714b72e2ed3b">IDirect3DSurface9::GetDC</a>. Otherwise, this method will fail.




## -see-also




<a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>



<a href="https://msdn.microsoft.com/3456470b-60c5-4ac2-bb71-714b72e2ed3b">IDirect3DSurface9::GetDC</a>
 

 

