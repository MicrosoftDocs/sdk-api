---
UID: NF:d3d9helper.IDirect3DDevice9.GetNumberOfSwapChains
title: IDirect3DDevice9::GetNumberOfSwapChains
author: windows-sdk-content
description: Gets the number of implicit swap chains.
old-location: direct3d9\idirect3ddevice9__getnumberofswapchains.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getnumberofswapchains.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 84771686-c1f5-0be3-b170-1de4e0c8acc9, GetNumberOfSwapChains, GetNumberOfSwapChains method [Direct3D 9], GetNumberOfSwapChains method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetNumberOfSwapChains method, IDirect3DDevice9.GetNumberOfSwapChains, IDirect3DDevice9::GetNumberOfSwapChains, d3d9helper/IDirect3DDevice9::GetNumberOfSwapChains, direct3d9.idirect3ddevice9__getnumberofswapchains
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.GetNumberOfSwapChains
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetNumberOfSwapChains


## -description


Gets the number of implicit swap chains.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of implicit swap chains. See Remarks.




## -remarks



Implicit swap chains are created by the device during <a href="https://msdn.microsoft.com/library/Bb174313(v=VS.85).aspx">IDirect3D9::CreateDevice</a>. This method returns the number of swap chains created by CreateDevice. 
    


An application may create additional swap chains using <a href="https://msdn.microsoft.com/library/Bb174354(v=VS.85).aspx">IDirect3DDevice9::CreateAdditionalSwapChain</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

