---
UID: NN:dxgi1_3.IDXGIOutput2
title: IDXGIOutput2 (dxgi1_3.h)
description: Represents an adapter output (such as a monitor). The IDXGIOutput2 interface exposes a method to check for multiplane overlay support on the primary output adapter.
helpviewer_keywords: ["IDXGIOutput2","IDXGIOutput2 interface [DXGI]","IDXGIOutput2 interface [DXGI]","described","direct3ddxgi.idxgioutput2","dxgi1_3/IDXGIOutput2"]
old-location: direct3ddxgi\idxgioutput2.htm
tech.root: direct3ddxgi
ms.assetid: 23585A1F-3F18-4247-91DB-712C0A8D5398
ms.date: 12/05/2018
ms.keywords: IDXGIOutput2, IDXGIOutput2 interface [DXGI], IDXGIOutput2 interface [DXGI],described, direct3ddxgi.idxgioutput2, dxgi1_3/IDXGIOutput2
req.header: dxgi1_3.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput2
 - dxgi1_3/IDXGIOutput2
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
 - IDXGIOutput2
---

# IDXGIOutput2 interface


## -description

Represents an adapter output (such as a monitor). The <b>IDXGIOutput2</b> interface exposes a method to check for multiplane overlay support on the primary output adapter.

## -inheritance

The <b>IDXGIOutput2</b> interface inherits from <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1">IDXGIOutput1</a>. <b>IDXGIOutput2</b> also has these types of members:

## -remarks

To determine  the outputs that are available from the adapter, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs">IDXGIAdapter::EnumOutputs</a>. To determine the specific output that the swap chain will update, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">IDXGISwapChain::GetContainingOutput</a>. You can then call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> from any  <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> or <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1">IDXGIOutput1</a> object to obtain an <b>IDXGIOutput2</b> object.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1">IDXGIOutput1</a>
