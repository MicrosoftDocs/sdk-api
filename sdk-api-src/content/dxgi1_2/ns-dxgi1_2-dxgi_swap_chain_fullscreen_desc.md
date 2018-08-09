---
UID: NS:dxgi1_2.DXGI_SWAP_CHAIN_FULLSCREEN_DESC
title: DXGI_SWAP_CHAIN_FULLSCREEN_DESC
author: windows-sdk-content
description: Describes full-screen mode for a swap chain.
old-location: direct3ddxgi\dxgi_swap_chain_fullscreen_desc.htm
old-project: direct3ddxgi
ms.assetid: 0EE5683E-0623-4FD7-A77F-B64F90A25C6A
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DXGI_SWAP_CHAIN_FULLSCREEN_DESC, DXGI_SWAP_CHAIN_FULLSCREEN_DESC structure [DXGI], direct3ddxgi.dxgi_swap_chain_fullscreen_desc, dxgi1_2/DXGI_SWAP_CHAIN_FULLSCREEN_DESC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXGI_SWAP_CHAIN_FULLSCREEN_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_SWAP_CHAIN_FULLSCREEN_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_SWAP_CHAIN_FULLSCREEN_DESC structure


## -description


Describes full-screen mode for a swap chain.


## -struct-fields




### -field RefreshRate

A <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure that describes the refresh rate in hertz.


### -field ScanlineOrdering

A member of the <a href="https://msdn.microsoft.com/ecb66eed-9368-4cac-82e9-0e32c41e3ec5">DXGI_MODE_SCANLINE_ORDER</a> enumerated type that describes the scan-line drawing mode.


### -field Scaling

A member of the <a href="https://msdn.microsoft.com/2f9c16c6-b2d2-4135-8399-fd37aece3286">DXGI_MODE_SCALING</a> enumerated type that describes the scaling mode.


### -field Windowed

A Boolean value that specifies whether the swap chain is in windowed mode. <b>TRUE</b> if the swap chain is in windowed mode; otherwise, <b>FALSE</b>.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">CreateSwapChainForHwnd</a> and <a href="https://msdn.microsoft.com/6056239A-B3CA-4C70-9081-499B0AAEFBEF">GetFullscreenDesc</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

