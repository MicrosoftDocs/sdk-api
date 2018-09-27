---
UID: NF:d3d9.IDirect3DSwapChain9Ex.GetLastPresentCount
title: IDirect3DSwapChain9Ex::GetLastPresentCount
author: windows-sdk-content
description: Returns the number of times the swapchain has been processed.
old-location: direct3d9\idirect3dswapchain9_getlastpresentcount.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9_getlastpresentcount.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetLastPresentCount, GetLastPresentCount method [Direct3D 9], GetLastPresentCount method [Direct3D 9],IDirect3DSwapChain9Ex interface, IDirect3DSwapChain9Ex interface [Direct3D 9],GetLastPresentCount method, IDirect3DSwapChain9Ex.GetLastPresentCount, IDirect3DSwapChain9Ex::GetLastPresentCount, d305fb15-e0d6-5a21-767a-ac221539a549, d3d9/IDirect3DSwapChain9Ex::GetLastPresentCount, direct3d9.idirect3dswapchain9_getlastpresentcount
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
 - IDirect3DSwapChain9Ex.GetLastPresentCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSwapChain9Ex::GetLastPresentCount


## -description


Returns the number of times the swapchain has been processed.


## -parameters




### -param pLastPresentCount [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to a UINT to be filled with the number of times the <a href="https://msdn.microsoft.com/en-us/library/Bb174343(v=VS.85).aspx">IDirect3DDevice9Ex::PresentEx</a> method has been called. The count will also be incremented by calling some other APIs such as <a href="https://msdn.microsoft.com/en-us/library/Bb174432(v=VS.85).aspx">IDirect3DDevice9::SetDialogBoxMode</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

S_OK the method was successful.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172503(v=VS.85).aspx">IDirect3DSwapChain9Ex</a>
 

 

