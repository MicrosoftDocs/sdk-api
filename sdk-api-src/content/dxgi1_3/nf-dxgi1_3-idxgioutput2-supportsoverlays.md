---
UID: NF:dxgi1_3.IDXGIOutput2.SupportsOverlays
title: IDXGIOutput2::SupportsOverlays
author: windows-sdk-content
description: Queries an adapter output for multiplane overlay support.
old-location: direct3ddxgi\idxgioutput2_supportsoverlays.htm
old-project: direct3ddxgi
ms.assetid: BC9CD287-CD89-4D0C-ADE3-EAA60D5FEAAD
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IDXGIOutput2 interface [DXGI],SupportsOverlays method, IDXGIOutput2.SupportsOverlays, IDXGIOutput2::SupportsOverlays, SupportsOverlays, SupportsOverlays method [DXGI], SupportsOverlays method [DXGI],IDXGIOutput2 interface, direct3ddxgi.idxgioutput2_supportsoverlays, dxgi1_3/IDXGIOutput2::SupportsOverlays
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
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
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput2::SupportsOverlays


## -description


Queries an adapter output for multiplane overlay support. If this API returns ‘TRUE’, multiple swap chain composition takes place in a performant manner using overlay hardware. If this API returns false, apps should avoid using foreground swap chains (that is, avoid using swap chains created with the <a href="https://msdn.microsoft.com/library/Bb173076(v=VS.85).aspx">DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER</a> flag).


## -parameters






## -returns



TRUE if the output adapter is the primary adapter and it supports multiplane overlays, otherwise returns FALSE.




## -remarks



See <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">CreateSwapChainForCoreWindow</a> for info on creating a foreground swap chain.




## -see-also




<a href="https://msdn.microsoft.com/23585A1F-3F18-4247-91DB-712C0A8D5398">IDXGIOutput2</a>
 

 

