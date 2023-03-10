---
UID: NN:dxgidebug.IDXGIDebug1
title: IDXGIDebug1 (dxgidebug.h)
description: Controls debug settings for Microsoft DirectX Graphics Infrastructure (DXGI). You can use the IDXGIDebug1 interface in Windows Store apps.
helpviewer_keywords: ["IDXGIDebug1","IDXGIDebug1 interface [DXGI]","IDXGIDebug1 interface [DXGI]","described","direct3ddxgi.idxgidebug1","dxgidebug/IDXGIDebug1"]
old-location: direct3ddxgi\idxgidebug1.htm
tech.root: direct3ddxgi
ms.assetid: 16D52CA2-1495-407C-9B88-CF4D4C90BAFA
ms.date: 12/05/2018
ms.keywords: IDXGIDebug1, IDXGIDebug1 interface [DXGI], IDXGIDebug1 interface [DXGI],described, direct3ddxgi.idxgidebug1, dxgidebug/IDXGIDebug1
req.header: dxgidebug.h
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
req.lib: 
req.dll: DXGIDebug.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDebug1
 - dxgidebug/IDXGIDebug1
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
 - IDXGIDebug1
---

# IDXGIDebug1 interface


## -description

Controls debug settings for Microsoft DirectX Graphics Infrastructure (DXGI). You can use the  <b>IDXGIDebug1</b> interface in Windows Store apps.

## -inheritance

The <b>IDXGIDebug1</b> interface inherits from <a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a>. <b>IDXGIDebug1</b> also has these types of members:

## -remarks

Call the <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1">DXGIGetDebugInterface1</a> function to obtain the <b>IDXGIDebug1</b> interface.

The <b>IDXGIDebug1</b> interface can be used only if the debug layer is turned on. For more info, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">Debug Layer</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1">DXGIGetDebugInterface1</a>



<a href="/windows/desktop/api/dxgidebug/nn-dxgidebug-idxgidebug">IDXGIDebug</a>
