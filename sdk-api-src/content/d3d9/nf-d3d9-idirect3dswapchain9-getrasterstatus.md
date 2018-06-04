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

# IDirect3DSwapChain9::GetRasterStatus


## -description


Returns information describing the raster of the monitor on which the swap chain is presented.


## -parameters




### -param pRasterStatus [out]

Type: <b><a href="https://msdn.microsoft.com/f7b5b714-8fc8-47b8-adec-1089b8d07081">D3DRASTER_STATUS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/f7b5b714-8fc8-47b8-adec-1089b8d07081">D3DRASTER_STATUS</a> structure filled with information about the position or other status of the raster on the monitor driven by this adapter. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if pRasterStatus is invalid or if the device does not support reading the current scan line. To determine if the device supports reading the scan line, check for the D3DCAPS_READ_SCANLINE flag in the Caps member of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7b5b714-8fc8-47b8-adec-1089b8d07081">D3DRASTER_STATUS</a>



<a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>
 

 

