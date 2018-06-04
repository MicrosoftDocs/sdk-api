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

# IDXGIOutput2::SupportsOverlays


## -description


Queries an adapter output for multiplane overlay support. If this API returns ‘TRUE’, multiple swap chain composition takes place in a performant manner using overlay hardware. If this API returns false, apps should avoid using foreground swap chains (that is, avoid using swap chains created with the <a href="https://msdn.microsoft.com/c0030570-89ba-4586-a358-8c3b8c393a90">DXGI_SWAP_CHAIN_FLAG_FOREGROUND_LAYER</a> flag).


## -parameters






## -returns



TRUE if the output adapter is the primary adapter and it supports multiplane overlays, otherwise returns FALSE.




## -remarks



See <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">CreateSwapChainForCoreWindow</a> for info on creating a foreground swap chain.




## -see-also




<a href="https://msdn.microsoft.com/23585A1F-3F18-4247-91DB-712C0A8D5398">IDXGIOutput2</a>
 

 

