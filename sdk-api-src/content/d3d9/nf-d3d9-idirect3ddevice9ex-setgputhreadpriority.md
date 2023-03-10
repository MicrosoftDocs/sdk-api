---
UID: NF:d3d9.IDirect3DDevice9Ex.SetGPUThreadPriority
title: IDirect3DDevice9Ex::SetGPUThreadPriority (d3d9.h)
description: Set the priority on the GPU thread.
helpviewer_keywords: ["IDirect3DDevice9Ex interface [Direct3D 9]","SetGPUThreadPriority method","IDirect3DDevice9Ex.SetGPUThreadPriority","IDirect3DDevice9Ex::SetGPUThreadPriority","SetGPUThreadPriority","SetGPUThreadPriority method [Direct3D 9]","SetGPUThreadPriority method [Direct3D 9]","IDirect3DDevice9Ex interface","ac16f6ba-fdcc-9d18-4ea1-2b6b2313ab4a","d3d9/IDirect3DDevice9Ex::SetGPUThreadPriority","direct3d9.idirect3ddevice9ex_setgputhreadpriority"]
old-location: direct3d9\idirect3ddevice9ex_setgputhreadpriority.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_setgputhreadpriority.htm
ms.date: 12/05/2018
ms.keywords: IDirect3DDevice9Ex interface [Direct3D 9],SetGPUThreadPriority method, IDirect3DDevice9Ex.SetGPUThreadPriority, IDirect3DDevice9Ex::SetGPUThreadPriority, SetGPUThreadPriority, SetGPUThreadPriority method [Direct3D 9], SetGPUThreadPriority method [Direct3D 9],IDirect3DDevice9Ex interface, ac16f6ba-fdcc-9d18-4ea1-2b6b2313ab4a, d3d9/IDirect3DDevice9Ex::SetGPUThreadPriority, direct3d9.idirect3ddevice9ex_setgputhreadpriority
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9Ex::SetGPUThreadPriority
 - d3d9/IDirect3DDevice9Ex::SetGPUThreadPriority
dev_langs:
 - c++
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
---

# IDirect3DDevice9Ex::SetGPUThreadPriority


## -description

Set the priority on the GPU thread.

## -parameters

### -param Priority [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

The thread priority, ranging from -7 to 7.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_INVALIDCALL, or D3DERR_DEVICEREMOVED (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>).

## -remarks

GPU thread priority is not reset when a device is lost. The effects of calls to this method are not recorded in state blocks.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>