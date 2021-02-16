---
UID: NF:dxgi.IDXGIFactory.EnumAdapters
title: IDXGIFactory::EnumAdapters (dxgi.h)
description: Enumerates the adapters (video cards).
helpviewer_keywords: ["457b8c88-be8c-c241-7864-e16ac2622ee0","EnumAdapters","EnumAdapters method [DXGI]","EnumAdapters method [DXGI]","IDXGIFactory interface","IDXGIFactory interface [DXGI]","EnumAdapters method","IDXGIFactory.EnumAdapters","IDXGIFactory::EnumAdapters","direct3ddxgi.idxgifactory_enumadapters","dxgi/IDXGIFactory::EnumAdapters"]
old-location: direct3ddxgi\idxgifactory_enumadapters.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_enumadapters.htm
ms.date: 12/05/2018
ms.keywords: 457b8c88-be8c-c241-7864-e16ac2622ee0, EnumAdapters, EnumAdapters method [DXGI], EnumAdapters method [DXGI],IDXGIFactory interface, IDXGIFactory interface [DXGI],EnumAdapters method, IDXGIFactory.EnumAdapters, IDXGIFactory::EnumAdapters, direct3ddxgi.idxgifactory_enumadapters, dxgi/IDXGIFactory::EnumAdapters
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
 - IDXGIFactory::EnumAdapters
 - dxgi/IDXGIFactory::EnumAdapters
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
 - IDXGIFactory.EnumAdapters
---

# IDXGIFactory::EnumAdapters


## -description

Enumerates the adapters (video cards).

## -parameters

### -param Adapter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the adapter to enumerate.

### -param ppAdapter [out]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> interface at the position specified by the <i>Adapter</i> parameter.  This parameter must not be <b>NULL</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_FOUND</a> if the index is greater than or equal to the number of adapters in the local system, or <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if <i>ppAdapter</i> parameter is <b>NULL</b>.

## -remarks

When you create a factory, the factory enumerates the set of adapters that are available in the system. Therefore, if you change the adapters in a system, you must destroy 
      and recreate the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a> object. The number of adapters in a system changes when you add or remove a display card, or dock or undock a laptop. 

When the <b>EnumAdapters</b> method succeeds and fills the <i>ppAdapter</i> parameter with the address of the pointer to the adapter interface, <b>EnumAdapters</b> increments the adapter interface's reference count. When you finish using the 
      adapter interface, call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method to decrement the reference count before you destroy the pointer.

<b>EnumAdapters</b> first returns the adapter with the output on which the desktop primary is displayed. This adapter corresponds with an index of zero. <b>EnumAdapters</b> next returns other adapters with outputs. <b>EnumAdapters</b> finally returns adapters without outputs.




#### Examples

Enumerating Adapters
          

The following code example demonstrates how to enumerate adapters using the <b>EnumAdapters</b> method.


```

UINT i = 0; 
IDXGIAdapter * pAdapter; 
std::vector <IDXGIAdapter*> vAdapters; 
while(pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND) 
{ 
	vAdapters.push_back(pAdapter); 
	++i; 
} 

```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>