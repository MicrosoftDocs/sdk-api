---
UID: NF:d3d9.IDirect3D9.GetAdapterDisplayMode
title: IDirect3D9::GetAdapterDisplayMode
author: windows-sdk-content
description: Retrieves the current display mode of the adapter.
old-location: direct3d9\idirect3d9__getadapterdisplaymode.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getadapterdisplaymode.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: GetAdapterDisplayMode, GetAdapterDisplayMode method [Direct3D 9], GetAdapterDisplayMode method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetAdapterDisplayMode method, IDirect3D9.GetAdapterDisplayMode, IDirect3D9::GetAdapterDisplayMode, a03b5255-0046-403d-b90f-e76191710598, d3d9helper/IDirect3D9::GetAdapterDisplayMode, direct3d9.idirect3d9__getadapterdisplaymode
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
 - IDirect3D9.GetAdapterDisplayMode
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9::GetAdapterDisplayMode


## -description


Retrieves the current display mode of the adapter.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter to query. D3DADAPTER_DEFAULT is always the primary display adapter. 


### -param pMode [in, out]

Type: <b><a href="https://msdn.microsoft.com/e83c03ee-2067-45c9-8fd8-8c4db5558df4">D3DDISPLAYMODE</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/e83c03ee-2067-45c9-8fd8-8c4db5558df4">D3DDISPLAYMODE</a> structure, to be filled with information describing the current adapter's mode. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. 



If Adapter is out of range or pMode is invalid, this method returns D3DERR_INVALIDCALL.




## -remarks



<b>GetAdapterDisplayMode</b> will not return the correct format when the display is in an extended format, such as 2:10:10:10. Instead, it returns the format X8R8G8B8.
    





## -see-also




<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

