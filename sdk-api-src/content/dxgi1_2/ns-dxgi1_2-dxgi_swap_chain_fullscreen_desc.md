---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

