---
UID: NF:dxgi.IDXGIFactory.GetWindowAssociation
title: IDXGIFactory::GetWindowAssociation (dxgi.h)
description: Get the window through which the user controls the transition to and from full screen.
helpviewer_keywords: ["GetWindowAssociation","GetWindowAssociation method [DXGI]","GetWindowAssociation method [DXGI]","IDXGIFactory interface","IDXGIFactory interface [DXGI]","GetWindowAssociation method","IDXGIFactory.GetWindowAssociation","IDXGIFactory::GetWindowAssociation","b199d248-a0a8-e257-1b89-68baeb809572","direct3ddxgi.idxgifactory_getwindowassociation","dxgi/IDXGIFactory::GetWindowAssociation"]
old-location: direct3ddxgi\idxgifactory_getwindowassociation.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_getwindowassociation.htm
ms.date: 12/05/2018
ms.keywords: GetWindowAssociation, GetWindowAssociation method [DXGI], GetWindowAssociation method [DXGI],IDXGIFactory interface, IDXGIFactory interface [DXGI],GetWindowAssociation method, IDXGIFactory.GetWindowAssociation, IDXGIFactory::GetWindowAssociation, b199d248-a0a8-e257-1b89-68baeb809572, direct3ddxgi.idxgifactory_getwindowassociation, dxgi/IDXGIFactory::GetWindowAssociation
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
 - IDXGIFactory::GetWindowAssociation
 - dxgi/IDXGIFactory::GetWindowAssociation
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
 - IDXGIFactory.GetWindowAssociation
---

# IDXGIFactory::GetWindowAssociation


## -description

Get the window through which the user controls the transition to and from full screen.

## -parameters

### -param pWindowHandle [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a>*</b>

A pointer to a window handle.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns a code that indicates success or failure. <b>S_OK</b> indicates success, <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> indicates <i>pWindowHandle</i> was passed in as <b>NULL</b>.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>