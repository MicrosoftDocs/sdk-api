---
UID: NF:dxgi1_6.DXGIDeclareAdapterRemovalSupport
title: DXGIDeclareAdapterRemovalSupport function (dxgi1_6.h)
description: Allows a process to indicate that it's resilient to any of its graphics devices being removed.
helpviewer_keywords: ["DXGIDeclareAdapterRemovalSupport","DXGIDeclareAdapterRemovalSupport function [DXGI]","direct3ddxgi.dxgideclareadapterremovalsupport","dxgi1_6/DXGIDeclareAdapterRemovalSupport"]
old-location: direct3ddxgi\dxgideclareadapterremovalsupport.htm
tech.root: direct3ddxgi
ms.assetid: 602EA66C-6D3D-4604-822C-DBD66EB70C3C
ms.date: 12/05/2018
ms.keywords: DXGIDeclareAdapterRemovalSupport, DXGIDeclareAdapterRemovalSupport function [DXGI], direct3ddxgi.dxgideclareadapterremovalsupport, dxgi1_6/DXGIDeclareAdapterRemovalSupport
req.header: dxgi1_6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGIDeclareAdapterRemovalSupport
 - dxgi1_6/DXGIDeclareAdapterRemovalSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxgi.dll
api_name:
 - DXGIDeclareAdapterRemovalSupport
---

# DXGIDeclareAdapterRemovalSupport function


## -description

Allows a process to indicate that it's resilient to any of its graphics devices being removed.



## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful; an error code otherwise. If this function is called after device creation, it returns <b>DXGI_ERROR_INVALID_CALL</b>. If this is not the first time that this function is called, it returns <b>DXGI_ERROR_ALREADY_EXISTS</b>. For a full list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

This function is graphics API-agnostic, meaning that apps running on other APIs, such as OpenGL and Vulkan, would also apply.

This function should be called once per process and before any device creation.

## -see-also

<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Tools/DXGIAdapterRemovalSupportTest">DXGI AdapterRemovalSupport test sample</a>



<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-functions">DXGI Functions</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/UWP/D3D12xGPU">xGPU UWP sample</a>



<a href="https://github.com/Microsoft/DirectX-Graphics-Samples/tree/develop/Samples/Desktop/D3D12xGPU">xGPU desktop sample</a>
