---
UID: NF:dxgi.CreateDXGIFactory
title: CreateDXGIFactory function (dxgi.h)
description: Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.
helpviewer_keywords: ["CreateDXGIFactory","CreateDXGIFactory function [DXGI]","direct3ddxgi.createdxgifactory","dxgi/CreateDXGIFactory","f8906daa-c399-a76f-d487-e1f2ee03b8a8"]
old-location: direct3ddxgi\createdxgifactory.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\createdxgifactory.htm
ms.date: 12/05/2018
ms.keywords: CreateDXGIFactory, CreateDXGIFactory function [DXGI], direct3ddxgi.createdxgifactory, dxgi/CreateDXGIFactory, f8906daa-c399-a76f-d487-e1f2ee03b8a8
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
req.dll: DXGI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateDXGIFactory
 - dxgi/CreateDXGIFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DXGI.dll
api_name:
 - CreateDXGIFactory
---

# CreateDXGIFactory function


## -description

Creates a DXGI 1.0 factory that you can use to generate other  DXGI objects.

## -parameters

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a> object referenced by the <i>ppFactory</i> parameter.

### -param ppFactory [out]

Type: <b>void**</b>

Address of a pointer to an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a> object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

Use a DXGI factory to generate objects that <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">enumerate adapters</a>, <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">create swap chains</a>, and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation">associate a window</a> with the alt+enter key sequence for toggling to and from the fullscreen display mode.

If the <b>CreateDXGIFactory</b> function succeeds, the reference count on the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a> interface is incremented. To avoid a memory leak, when you finish using the interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IDXGIFactory::Release</a> method to release the interface.

<div class="alert"><b>Note</b>  Do not mix the use of DXGI 1.0 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>) and DXGI 1.1 (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>) in an application. Use <b>IDXGIFactory</b> or <b>IDXGIFactory1</b>, but not both in an application.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>CreateDXGIFactory</b> fails if your app's <a href="/windows/desktop/Dlls/dllmain">DllMain</a> function calls it. For more info about how DXGI responds from <b>DllMain</b>, see <a href="/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi">DXGI Responses from DLLMain</a>.</div>
<div> </div>
<div class="alert"><b>Note</b>  Starting with Windows 8, all DXGI factories (regardless if they were created with <b>CreateDXGIFactory</b> or <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a>) enumerate adapters identically. The enumeration order of adapters, which you retrieve with <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory::EnumAdapters</a> or <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1">IDXGIFactory1::EnumAdapters1</a>, is as follows: <ul>
<li>Adapter with the output on which the desktop primary is displayed. This adapter corresponds with an index of zero.</li>
<li>Adapters with outputs.</li>
<li>Adapters without outputs.</li>
</ul>
</div>
<div> </div>
The <b>CreateDXGIFactory</b> function does not exist for Windows Store apps. Instead, Windows Store apps use the  <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a> function.


#### Examples

Creating a DXGI 1.0 Factory
          

The following code example demonstrates how to create a DXGI 1.0 factory.  This example uses the __uuidof() intrinsic to obtain the REFIID, or GUID, of the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a> interface.


```

IDXGIFactory * pFactory;
HRESULT hr = CreateDXGIFactory(__uuidof(IDXGIFactory), (void**)(&pFactory) );

```

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-functions">DXGI Functions</a>