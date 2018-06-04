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

# IWICPalette::GetType


## -description


Retrieves the <a href="https://msdn.microsoft.com/a8192905-2bae-4760-bf2d-64640c46e168">WICBitmapPaletteType</a> that describes the palette. 


## -parameters




### -param pePaletteType [out]

Type: <b><a href="https://msdn.microsoft.com/a8192905-2bae-4760-bf2d-64640c46e168">WICBitmapPaletteType</a>*</b>

Pointer that receives the palette type of the bimtap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>WICBitmapPaletteCustom</b> is used for palettes initialized from both <a href="https://msdn.microsoft.com/eef17030-13eb-4d59-ac47-a49ffe2c80c8">InitializeCustom</a> and <a href="https://msdn.microsoft.com/f17d0f16-729e-466c-902f-61398daf2921">InitializeFromBitmap</a>. There is no distinction is made between optimized and custom palettes.



