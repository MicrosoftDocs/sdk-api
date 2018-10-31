---
UID: NF:d3d9.IDirect3DDevice9Ex.SetGPUThreadPriority
title: IDirect3DDevice9Ex::SetGPUThreadPriority
author: windows-sdk-content
description: Set the priority on the GPU thread.
old-location: direct3d9\idirect3ddevice9ex_setgputhreadpriority.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_setgputhreadpriority.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirect3DDevice9Ex interface [Direct3D 9],SetGPUThreadPriority method, IDirect3DDevice9Ex.SetGPUThreadPriority, IDirect3DDevice9Ex::SetGPUThreadPriority, SetGPUThreadPriority, SetGPUThreadPriority method [Direct3D 9], SetGPUThreadPriority method [Direct3D 9],IDirect3DDevice9Ex interface, ac16f6ba-fdcc-9d18-4ea1-2b6b2313ab4a, d3d9/IDirect3DDevice9Ex::SetGPUThreadPriority, direct3d9.idirect3ddevice9ex_setgputhreadpriority
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
 - IDirect3DDevice9Ex.SetGPUThreadPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9Ex::SetGPUThreadPriority


## -description


Set the priority on the GPU thread.


## -parameters




### -param Priority

TBD




#### - pPriority [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The thread priority, ranging from -7 to 7.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_INVALIDCALL, or D3DERR_DEVICEREMOVED (see <a href="https://msdn.microsoft.com/en-us/library/Bb172554(v=VS.85).aspx">D3DERR</a>).




## -remarks



GPU thread priority is not reset when a device is lost. The effects of calls to this method are not recorded in state blocks.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>
 

 

