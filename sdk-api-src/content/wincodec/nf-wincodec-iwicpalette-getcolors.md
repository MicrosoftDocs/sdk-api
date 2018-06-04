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

# IWICPalette::GetColors


## -description


Fills out the supplied color array with the colors from the internal color table. The color array should be sized according to the return results from <a href="https://msdn.microsoft.com/133ee983-8df2-4053-aa8a-471aa679b412">GetColorCount</a>.


## -parameters




### -param cCount




### -param pColors [out]

Type: <b>WICColor*</b>

Pointer that receives the colors of the palette.


### -param pcActualColors [out]

Type: <b>UINT*</b>

The actual size needed to obtain the palette colors.


#### - colorCount [in]

Type: <b>UINT</b>

The size of the <i>pColors</i> array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



