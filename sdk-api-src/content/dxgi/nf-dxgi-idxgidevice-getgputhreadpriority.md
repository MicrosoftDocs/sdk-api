---
UID: NF:dxgi.IDXGIDevice.GetGPUThreadPriority
title: IDXGIDevice::GetGPUThreadPriority (dxgi.h)
description: Gets the GPU thread priority.
helpviewer_keywords: ["GetGPUThreadPriority","GetGPUThreadPriority method [DXGI]","GetGPUThreadPriority method [DXGI]","IDXGIDevice interface","IDXGIDevice interface [DXGI]","GetGPUThreadPriority method","IDXGIDevice.GetGPUThreadPriority","IDXGIDevice::GetGPUThreadPriority","direct3ddxgi.idxgidevice_getgputhreadpriority","dxgi/IDXGIDevice::GetGPUThreadPriority","fbea5e3b-9023-68ed-7a86-b421d1d2cf36"]
old-location: direct3ddxgi\idxgidevice_getgputhreadpriority.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_getgputhreadpriority.htm
ms.date: 12/05/2018
ms.keywords: GetGPUThreadPriority, GetGPUThreadPriority method [DXGI], GetGPUThreadPriority method [DXGI],IDXGIDevice interface, IDXGIDevice interface [DXGI],GetGPUThreadPriority method, IDXGIDevice.GetGPUThreadPriority, IDXGIDevice::GetGPUThreadPriority, direct3ddxgi.idxgidevice_getgputhreadpriority, dxgi/IDXGIDevice::GetGPUThreadPriority, fbea5e3b-9023-68ed-7a86-b421d1d2cf36
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDevice::GetGPUThreadPriority
 - dxgi/IDXGIDevice::GetGPUThreadPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIDevice.GetGPUThreadPriority
---

# IDXGIDevice::GetGPUThreadPriority


## -description

Gets the GPU thread priority.

## -parameters

### -param pPriority [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a>*</b>

A pointer to a variable that receives a value that indicates the current GPU thread priority. The value will be between -7 and 7, inclusive, where 0 represents normal priority.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Return S_OK if successful; otherwise, returns E_POINTER if the <i>pPriority</i> parameter is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>