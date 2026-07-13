---
UID: NN:dxgi1_2.IDXGIOutput1
title: IDXGIOutput1 (dxgi1_2.h)
description: An IDXGIOutput1 interface represents an adapter output (such as a monitor).
helpviewer_keywords: ["IDXGIOutput1","IDXGIOutput1 interface [DXGI]","IDXGIOutput1 interface [DXGI]","described","direct3ddxgi.idxgioutput1","dxgi1_2/IDXGIOutput1"]
old-location: direct3ddxgi\idxgioutput1.htm
tech.root: direct3ddxgi
ms.assetid: 27C7BD34-0746-4D5F-A746-45FFEE5BCD31
ms.date: 12/05/2018
ms.keywords: IDXGIOutput1, IDXGIOutput1 interface [DXGI], IDXGIOutput1 interface [DXGI],described, direct3ddxgi.idxgioutput1, dxgi1_2/IDXGIOutput1
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGIOutput1
 - dxgi1_2/IDXGIOutput1
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
 - IDXGIOutput1
---

# IDXGIOutput1 interface


## -description

An <b>IDXGIOutput1</b> interface represents an adapter output (such as a monitor).

## -inheritance

The <b>IDXGIOutput1</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>. <b>IDXGIOutput1</b> also has these types of members:

## -remarks

To determine  the outputs that are available from the adapter, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs">IDXGIAdapter::EnumOutputs</a>. To determine the specific output that the swap chain will update, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">IDXGISwapChain::GetContainingOutput</a>. You can then call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> from any  <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> object to obtain an <b>IDXGIOutput1</b> object.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
