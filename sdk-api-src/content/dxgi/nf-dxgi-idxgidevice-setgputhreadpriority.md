---
UID: NF:dxgi.IDXGIDevice.SetGPUThreadPriority
title: IDXGIDevice::SetGPUThreadPriority (dxgi.h)
description: Sets the GPU thread priority.
helpviewer_keywords: ["IDXGIDevice interface [DXGI]","SetGPUThreadPriority method","IDXGIDevice.SetGPUThreadPriority","IDXGIDevice::SetGPUThreadPriority","SetGPUThreadPriority","SetGPUThreadPriority method [DXGI]","SetGPUThreadPriority method [DXGI]","IDXGIDevice interface","b610ce23-f003-9031-4c67-b5013c5af229","direct3ddxgi.idxgidevice_setgputhreadpriority","dxgi/IDXGIDevice::SetGPUThreadPriority"]
old-location: direct3ddxgi\idxgidevice_setgputhreadpriority.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_setgputhreadpriority.htm
ms.date: 12/05/2018
ms.keywords: IDXGIDevice interface [DXGI],SetGPUThreadPriority method, IDXGIDevice.SetGPUThreadPriority, IDXGIDevice::SetGPUThreadPriority, SetGPUThreadPriority, SetGPUThreadPriority method [DXGI], SetGPUThreadPriority method [DXGI],IDXGIDevice interface, b610ce23-f003-9031-4c67-b5013c5af229, direct3ddxgi.idxgidevice_setgputhreadpriority, dxgi/IDXGIDevice::SetGPUThreadPriority
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
 - IDXGIDevice::SetGPUThreadPriority
 - dxgi/IDXGIDevice::SetGPUThreadPriority
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
 - IDXGIDevice.SetGPUThreadPriority
---

# IDXGIDevice::SetGPUThreadPriority


## -description

Sets the GPU thread priority.

## -parameters

### -param Priority

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

A value that specifies the required GPU thread priority. This value must be between -7 and 7, inclusive, where 0 represents normal priority.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Return S_OK if successful; otherwise, returns E_INVALIDARG if the <i>Priority</i> parameter is invalid.

## -remarks

The values for the <i>Priority</i> parameter function as follows:

<ul>
<li>Positive values increase the likelihood that the GPU scheduler will grant GPU execution cycles to the device when rendering.</li>
<li>Negative values lessen the likelihood that the device will receive GPU execution cycles when devices compete for them.</li>
<li>The device is guaranteed to receive some GPU execution cycles at all settings.</li>
</ul>
To use the <b>SetGPUThreadPriority</b> method, you should have a comprehensive understanding of GPU scheduling. You should profile your application to ensure that it behaves as intended. If used inappropriately, the <b>SetGPUThreadPriority</b> method can impede rendering speed and result in a poor user experience.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getgputhreadpriority">IDXGIDevice::GetGPUThreadPriority</a>