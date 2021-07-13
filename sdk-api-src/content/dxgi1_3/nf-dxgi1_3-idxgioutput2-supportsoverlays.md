---
UID: NF:dxgi1_3.IDXGIOutput2.SupportsOverlays
title: IDXGIOutput2::SupportsOverlays (dxgi1_3.h)
description: Queries an adapter output for multiplane overlay support.
helpviewer_keywords: ["IDXGIOutput2 interface [DXGI]","SupportsOverlays method","IDXGIOutput2.SupportsOverlays","IDXGIOutput2::SupportsOverlays","SupportsOverlays","SupportsOverlays method [DXGI]","SupportsOverlays method [DXGI]","IDXGIOutput2 interface","direct3ddxgi.idxgioutput2_supportsoverlays","dxgi1_3/IDXGIOutput2::SupportsOverlays"]
old-location: direct3ddxgi\idxgioutput2_supportsoverlays.htm
tech.root: direct3ddxgi
ms.assetid: BC9CD287-CD89-4D0C-ADE3-EAA60D5FEAAD
ms.date: 12/05/2018
ms.keywords: IDXGIOutput2 interface [DXGI],SupportsOverlays method, IDXGIOutput2.SupportsOverlays, IDXGIOutput2::SupportsOverlays, SupportsOverlays, SupportsOverlays method [DXGI], SupportsOverlays method [DXGI],IDXGIOutput2 interface, direct3ddxgi.idxgioutput2_supportsoverlays, dxgi1_3/IDXGIOutput2::SupportsOverlays
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput2::SupportsOverlays
 - dxgi1_3/IDXGIOutput2::SupportsOverlays
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutput2.SupportsOverlays
---

# IDXGIOutput2::SupportsOverlays


## -description

Queries an adapter output for multiplane overlay support. If this API returns ‘TRUE’, multiple swap chain composition takes place in a performant manner using overlay hardware. If this API returns false, apps should avoid using foreground swap chains (that is, avoid using swap chains created with the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER</a> flag).



## -returns

TRUE if the output adapter is the primary adapter and it supports multiplane overlays, otherwise returns FALSE.

## -remarks

See <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">CreateSwapChainForCoreWindow</a> for info on creating a foreground swap chain.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgioutput2">IDXGIOutput2</a>
