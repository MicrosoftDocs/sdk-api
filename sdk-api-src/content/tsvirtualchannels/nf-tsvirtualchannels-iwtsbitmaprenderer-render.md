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

# IWTSBitmapRenderer::Render


## -description


Called by a dynamic virtual channel plug-in to render bitmaps.


## -parameters




### -param imageFormat [in]

Specifies the format of the data in the <i>pImageBuffer</i> buffer. This parameter is ignored and only bitmaps can be rendered.


### -param dwWidth [in]

The width of the bitmap.


### -param dwHeight [in]

The height of the bitmap.


### -param cbStride [in]

The stride width of the bitmap.


### -param cbImageBuffer [in]

The size, in bytes, of the <i>pImageBuffer</i> buffer.


### -param pImageBuffer [in]

An array of bytes that contains the data to render.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6930683e-bb9e-499c-b44f-27938faff3db">IWTSBitmapRenderer</a>
 

 

