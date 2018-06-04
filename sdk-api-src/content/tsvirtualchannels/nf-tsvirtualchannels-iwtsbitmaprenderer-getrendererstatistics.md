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

# IWTSBitmapRenderer::GetRendererStatistics


## -description


Retrieves statistics for the RemoteFX media redirection bitmap renderer.


## -parameters




### -param pStatistics [out]

Type: <b><a href="https://msdn.microsoft.com/111FA0B3-BFC1-4BD7-8BF0-C0C746A39C5D">BITMAP_RENDERER_STATISTICS</a>*</b>

The address of a 
      <a href="https://msdn.microsoft.com/111FA0B3-BFC1-4BD7-8BF0-C0C746A39C5D">BITMAP_RENDERER_STATISTICS</a> structure 
      that receives the bitmap rendering statistics.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/111FA0B3-BFC1-4BD7-8BF0-C0C746A39C5D">BITMAP_RENDERER_STATISTICS</a>



<a href="https://msdn.microsoft.com/6930683e-bb9e-499c-b44f-27938faff3db">IWTSBitmapRenderer</a>
 

 

