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

# IWICBitmapFrameEncode::SetPalette


## -description


Sets the <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> for indexed pixel formats.


## -parameters




### -param pIPalette [in]

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>*</b>

The <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> to use for indexed pixel formats.

The encoder may change the palette to reflect the pixel formats the encoder supports.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method doesn't fail if called on a frame whose pixel format is set to a non-indexed pixel format. If the target pixel format is a non-indexed format, the palette will be ignored.

If you already called <a href="https://msdn.microsoft.com/9310f407-d310-402b-bd90-ebc7e8d99361">IWICBitmapEncoder::SetPalette</a> to set a global palette, this method overrides that palette for the current frame.

The palette must be specified before your first call to <a href="https://msdn.microsoft.com/57DB1340-9BE4-46ED-9ADE-9B91657F09B7">WritePixels</a>/<a href="https://msdn.microsoft.com/bc748982-6dc8-41cc-a23b-9d127dc22a1f">WriteSource</a>. Doing so will cause <b>WriteSource</b> to use the specified palette when converting the source image to the encoder pixel format. If no palette is specified, a palette will be generated on the first call to <b>WriteSource</b>.




