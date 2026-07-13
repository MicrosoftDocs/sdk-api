---
UID: NF:dxgi1_3.DXGIGetDebugInterface1
title: DXGIGetDebugInterface1 function (dxgi1_3.h)
description: Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).
helpviewer_keywords: ["DXGIGetDebugInterface1","DXGIGetDebugInterface1 function [DXGI]","direct3ddxgi.dxgigetdebuginterface1","dxgi1_3/DXGIGetDebugInterface1"]
old-location: direct3ddxgi\dxgigetdebuginterface1.htm
tech.root: direct3ddxgi
ms.assetid: 0FE0EAF5-3ADC-426F-9DA9-FEDEC519EEF0
ms.date: 12/05/2018
ms.keywords: DXGIGetDebugInterface1, DXGIGetDebugInterface1 function [DXGI], direct3ddxgi.dxgigetdebuginterface1, dxgi1_3/DXGIGetDebugInterface1
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - DXGIGetDebugInterface1
 - dxgi1_3/DXGIGetDebugInterface1
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
 - DXGIGetDebugInterface1
---

# DXGIGetDebugInterface1 function


## -description

Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).

## -parameters

### -param Flags

Not used.

### -param riid

The globally unique identifier (GUID) of the requested interface type, which can be the identifier for the <a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a>, <a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug1">IDXGIDebug1</a>, or <a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgiinfoqueue">IDXGIInfoQueue</a> interfaces.

### -param pDebug [out]

A pointer to a buffer that receives a pointer to the debugging interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>DXGIGetDebugInterface1</b> function returns  <b>E_NOINTERFACE</b> on systems without the Windows Software Development Kit (SDK) installed, because it's a development-time aid.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-functions">DXGI Functions</a>



<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug1">IDXGIDebug1</a>