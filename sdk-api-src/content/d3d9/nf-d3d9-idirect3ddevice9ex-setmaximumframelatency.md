---
UID: NF:d3d9.IDirect3DDevice9Ex.SetMaximumFrameLatency
title: IDirect3DDevice9Ex::SetMaximumFrameLatency
author: windows-sdk-content
description: Set the number of frames that the system is allowed to queue for rendering.
old-location: direct3d9\idirect3ddevice9ex_setmaximumframelatency.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_setmaximumframelatency.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirect3DDevice9Ex interface [Direct3D 9],SetMaximumFrameLatency method, IDirect3DDevice9Ex.SetMaximumFrameLatency, IDirect3DDevice9Ex::SetMaximumFrameLatency, SetMaximumFrameLatency, SetMaximumFrameLatency method [Direct3D 9], SetMaximumFrameLatency method [Direct3D 9],IDirect3DDevice9Ex interface, d3d9/IDirect3DDevice9Ex::SetMaximumFrameLatency, dec92ba9-626f-0377-78d2-9951aefa48b5, direct3d9.idirect3ddevice9ex_setmaximumframelatency
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
 - IDirect3DDevice9Ex.SetMaximumFrameLatency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9Ex::SetMaximumFrameLatency


## -description


Set the number of frames that the system is allowed to queue for rendering.


## -parameters




### -param MaxLatency [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The maximum number of back buffer frames that a driver can queue. The value is typically 3, but can range from 1 to 20. A value of 0 will reset latency to the default. For multi-head devices, <i>MaxLatency</i> is specified per-head.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Possible return values include: D3D_OK or D3DERR_DEVICEREMOVED (see <a href="https://msdn.microsoft.com/en-us/library/Bb172554(v=VS.85).aspx">D3DERR</a>).




## -remarks



Frame latency is the number of frames that are allowed to be stored in a queue, before submission for rendering. Latency is often used to control how the CPU chooses between responding to user input and frames that are in the render queue.

It is often beneficial for applications that have no user input (for example, video playback) to queue more than 3 frames of data.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>
 

 

