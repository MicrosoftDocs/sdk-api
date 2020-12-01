---
UID: NF:d3d9.IDirect3DDevice9Ex.GetGPUThreadPriority
title: IDirect3DDevice9Ex::GetGPUThreadPriority (d3d9.h)
description: Get the priority of the GPU thread.
helpviewer_keywords: ["GetGPUThreadPriority","GetGPUThreadPriority method [Direct3D 9]","GetGPUThreadPriority method [Direct3D 9]","IDirect3DDevice9Ex interface","IDirect3DDevice9Ex interface [Direct3D 9]","GetGPUThreadPriority method","IDirect3DDevice9Ex.GetGPUThreadPriority","IDirect3DDevice9Ex::GetGPUThreadPriority","d3d9/IDirect3DDevice9Ex::GetGPUThreadPriority","direct3d9.idirect3ddevice9ex_getgputhreadpriority","f7f920d1-5b01-e016-bbe8-663d05696c0e"]
old-location: direct3d9\idirect3ddevice9ex_getgputhreadpriority.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_getgputhreadpriority.htm
ms.date: 12/05/2018
ms.keywords: GetGPUThreadPriority, GetGPUThreadPriority method [Direct3D 9], GetGPUThreadPriority method [Direct3D 9],IDirect3DDevice9Ex interface, IDirect3DDevice9Ex interface [Direct3D 9],GetGPUThreadPriority method, IDirect3DDevice9Ex.GetGPUThreadPriority, IDirect3DDevice9Ex::GetGPUThreadPriority, d3d9/IDirect3DDevice9Ex::GetGPUThreadPriority, direct3d9.idirect3ddevice9ex_getgputhreadpriority, f7f920d1-5b01-e016-bbe8-663d05696c0e
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
 - IDirect3DDevice9Ex::GetGPUThreadPriority
 - d3d9/IDirect3DDevice9Ex::GetGPUThreadPriority
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
 - IDirect3DDevice9Ex.GetGPUThreadPriority
---

# IDirect3DDevice9Ex::GetGPUThreadPriority


## -description

Get the priority of the GPU thread.

## -parameters

### -param pPriority

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a>*</b>

Current GPU priority. Valid values range from -7 to 7.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: D3D_OK or D3DERR_DEVICEREMOVED (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>).

## -remarks

Use <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setgputhreadpriority">IDirect3DDevice9Ex::SetGPUThreadPriority</a> to set the priority of a thread.

This method will retrieve the priority of the thread stored with the Direct3D device even if it was created with the <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE_PUREDEVICE</a> flag.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>