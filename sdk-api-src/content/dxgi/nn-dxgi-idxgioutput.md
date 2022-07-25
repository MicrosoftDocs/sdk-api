---
UID: NN:dxgi.IDXGIOutput
title: IDXGIOutput (dxgi.h)
description: An IDXGIOutput interface represents an adapter output (such as a monitor).
helpviewer_keywords: ["1d09c573-df6d-db81-0dbe-3135c4704ef8","IDXGIOutput","IDXGIOutput interface [DXGI]","IDXGIOutput interface [DXGI]","described","direct3ddxgi.idxgioutput","dxgi/IDXGIOutput"]
old-location: direct3ddxgi\idxgioutput.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput.htm
ms.date: 12/05/2018
ms.keywords: 1d09c573-df6d-db81-0dbe-3135c4704ef8, IDXGIOutput, IDXGIOutput interface [DXGI], IDXGIOutput interface [DXGI],described, direct3ddxgi.idxgioutput, dxgi/IDXGIOutput
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
 - IDXGIOutput
 - dxgi/IDXGIOutput
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
 - IDXGIOutput
---

# IDXGIOutput interface


## -description

An <b>IDXGIOutput</b> interface represents an adapter output (such as a monitor).

## -inheritance

The <b>IDXGIOutput</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIOutput</b> also has these types of members:

## -remarks

To see the outputs available, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs">IDXGIAdapter::EnumOutputs</a>. To see the specific output that the swap chain will update, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">IDXGISwapChain::GetContainingOutput</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
