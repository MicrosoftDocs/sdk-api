---
UID: NN:dxgidebug.IDXGIInfoQueue
title: IDXGIInfoQueue (dxgidebug.h)
description: This interface controls the debug information queue, and can only be used if the debug layer is turned on.
helpviewer_keywords: ["IDXGIInfoQueue","IDXGIInfoQueue interface [DXGI]","IDXGIInfoQueue interface [DXGI]","described","direct3ddxgi.idxgiinfoqueue","dxgidebug/IDXGIInfoQueue"]
old-location: direct3ddxgi\idxgiinfoqueue.htm
tech.root: direct3ddxgi
ms.assetid: F1BC6752-F334-4E8C-BE42-B731635A799D
ms.date: 12/05/2018
ms.keywords: IDXGIInfoQueue, IDXGIInfoQueue interface [DXGI], IDXGIInfoQueue interface [DXGI],described, direct3ddxgi.idxgiinfoqueue, dxgidebug/IDXGIInfoQueue
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
 - IDXGIInfoQueue
 - dxgidebug/IDXGIInfoQueue
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
 - IDXGIInfoQueue
---

# IDXGIInfoQueue interface


## -description

This interface controls the debug information queue, and can only be used if the debug layer is turned on.

## -inheritance

The <b>IDXGIInfoQueue</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGIInfoQueue</b> also has these types of members:

## -remarks

This interface is obtained by calling the <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-dxgigetdebuginterface">DXGIGetDebugInterface</a> function.

For more info about the debug layer, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">Debug Layer</a>.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
