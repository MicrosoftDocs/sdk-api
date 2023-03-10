---
UID: NF:dxgi.IDXGIResource.GetUsage
title: IDXGIResource::GetUsage (dxgi.h)
description: Get the expected resource usage.
helpviewer_keywords: ["1fc82eef-f409-1d78-ab65-dd0124809d16","GetUsage","GetUsage method [DXGI]","GetUsage method [DXGI]","IDXGIResource interface","IDXGIResource interface [DXGI]","GetUsage method","IDXGIResource.GetUsage","IDXGIResource::GetUsage","direct3ddxgi.idxgiresource_getusage","dxgi/IDXGIResource::GetUsage"]
old-location: direct3ddxgi\idxgiresource_getusage.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource_getusage.htm
ms.date: 12/05/2018
ms.keywords: 1fc82eef-f409-1d78-ab65-dd0124809d16, GetUsage, GetUsage method [DXGI], GetUsage method [DXGI],IDXGIResource interface, IDXGIResource interface [DXGI],GetUsage method, IDXGIResource.GetUsage, IDXGIResource::GetUsage, direct3ddxgi.idxgiresource_getusage, dxgi/IDXGIResource::GetUsage
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
 - IDXGIResource::GetUsage
 - dxgi/IDXGIResource::GetUsage
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
 - IDXGIResource.GetUsage
---

# IDXGIResource::GetUsage


## -description

Get the expected resource usage.

## -parameters

### -param pUsage

Type: <b><a href="/windows/desktop/direct3ddxgi/dxgi-usage">DXGI_USAGE</a>*</b>

A pointer to a usage flag (see <a href="/windows/desktop/direct3ddxgi/dxgi-usage">DXGI_USAGE</a>). For Direct3D 10, a surface can be used as a shader input or a render-target output.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a>