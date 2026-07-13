---
UID: NF:dxgi1_3.CreateDXGIFactory2
title: CreateDXGIFactory2 function (dxgi1_3.h)
description: Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.
helpviewer_keywords: ["CreateDXGIFactory2","CreateDXGIFactory2 function [DXGI]","direct3ddxgi.createdxgifactory2","dxgi1_3/CreateDXGIFactory2"]
old-location: direct3ddxgi\createdxgifactory2.htm
tech.root: direct3ddxgi
ms.assetid: D3CF43B0-8F17-486E-8750-CF0B9052BE74
ms.date: 12/05/2018
ms.keywords: CreateDXGIFactory2, CreateDXGIFactory2 function [DXGI], direct3ddxgi.createdxgifactory2, dxgi1_3/CreateDXGIFactory2
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateDXGIFactory2
 - dxgi1_3/CreateDXGIFactory2
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
 - CreateDXGIFactory2
---

## -description

Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.

In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it. Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead. Use <b>CreateDXGIFactory2</b> and specify the DXGI_CREATE_FACTORY_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.

## -parameters

### -param Flags

Type: <b>UINT</b>

Valid values include the <b>DXGI_CREATE_FACTORY_DEBUG (0x01)</b> flag, and zero.

<div class="alert"><b>Note</b>  This flag will be set by the D3D runtime if:<ul>
<li>The system creates an implicit factory during device creation.</li>
<li>The D3D11_CREATE_DEVICE_DEBUG flag is specified during device creation, for example using <a href="/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a> (or the swapchain method, or the Direct3D 10 equivalents).</li>
</ul>
</div>
<div> </div>

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="/windows/win32/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a> object referenced by 
          the <i>ppFactory</i> parameter.

### -param ppFactory [out]

Type: <b>void**</b>

Address of a pointer to an [IDXGIFactory2](/windows/win32/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

This function accepts a flag indicating whether DXGIDebug.dll is loaded. The function otherwise behaves identically to <a href="/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-functions">DXGI Functions</a>
