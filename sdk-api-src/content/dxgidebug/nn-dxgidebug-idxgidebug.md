---
UID: NN:dxgidebug.IDXGIDebug
title: IDXGIDebug (dxgidebug.h)
description: This interface controls debug settings, and can only be used if the debug layer is turned on.
helpviewer_keywords: ["IDXGIDebug","IDXGIDebug interface [DXGI]","IDXGIDebug interface [DXGI]","described","direct3ddxgi.idxgidebug","dxgidebug/IDXGIDebug"]
old-location: direct3ddxgi\idxgidebug.htm
tech.root: direct3ddxgi
ms.assetid: 7DCA4750-A397-4B5A-908F-A046427D30FB
ms.date: 12/05/2018
ms.keywords: IDXGIDebug, IDXGIDebug interface [DXGI], IDXGIDebug interface [DXGI],described, direct3ddxgi.idxgidebug, dxgidebug/IDXGIDebug
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
 - IDXGIDebug
 - dxgidebug/IDXGIDebug
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
 - IDXGIDebug
---

# IDXGIDebug interface


## -description

This interface controls debug settings, and can only be used if the debug layer is turned on.

## -inheritance

The <b>IDXGIDebug</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGIDebug</b> also has these types of members:

## -remarks

This interface is obtained by calling the <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-dxgigetdebuginterface">DXGIGetDebugInterface</a> function.
        

For more info about the debug layer, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">Debug Layer</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.
      

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
