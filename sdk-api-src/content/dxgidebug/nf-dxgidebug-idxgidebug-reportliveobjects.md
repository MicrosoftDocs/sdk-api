---
UID: NF:dxgidebug.IDXGIDebug.ReportLiveObjects
title: IDXGIDebug::ReportLiveObjects (dxgidebug.h)
description: Reports info about the lifetime of an object or objects.
helpviewer_keywords: ["IDXGIDebug interface [DXGI]","ReportLiveObjects method","IDXGIDebug.ReportLiveObjects","IDXGIDebug::ReportLiveObjects","ReportLiveObjects","ReportLiveObjects method [DXGI]","ReportLiveObjects method [DXGI]","IDXGIDebug interface","direct3ddxgi.idxgidebug_reportliveobjects","dxgidebug/IDXGIDebug::ReportLiveObjects"]
old-location: direct3ddxgi\idxgidebug_reportliveobjects.htm
tech.root: direct3ddxgi
ms.assetid: 6CA5C335-08E3-4CC6-A9C9-D7BC6B11C0EA
ms.date: 12/05/2018
ms.keywords: IDXGIDebug interface [DXGI],ReportLiveObjects method, IDXGIDebug.ReportLiveObjects, IDXGIDebug::ReportLiveObjects, ReportLiveObjects, ReportLiveObjects method [DXGI], ReportLiveObjects method [DXGI],IDXGIDebug interface, direct3ddxgi.idxgidebug_reportliveobjects, dxgidebug/IDXGIDebug::ReportLiveObjects
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDebug::ReportLiveObjects
 - dxgidebug/IDXGIDebug::ReportLiveObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGIDebug.dll
api_name:
 - IDXGIDebug.ReportLiveObjects
---

## -description

Reports info about the lifetime of an object or objects.

See the [Memory management sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/TechniqueDemos/D3D12MemoryManagement).

## -parameters

### -param apiid

The globally unique identifier (GUID) of the object or objects to get info about. Use one of the <a href="/windows/desktop/direct3ddxgi/dxgi-debug-id">DXGI_DEBUG_ID</a> GUIDs.

### -param flags

A <a href="/windows/desktop/api/dxgidebug/ne-dxgidebug-dxgi_debug_rlo_flags">DXGI_DEBUG_RLO_FLAGS</a>-typed value that specifies the amount of info to report.

## -returns

Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a>

[Memory management sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/TechniqueDemos/D3D12MemoryManagement)
