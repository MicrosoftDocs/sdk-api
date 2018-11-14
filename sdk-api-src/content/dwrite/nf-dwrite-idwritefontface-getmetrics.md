---
UID: NF:dwrite.IDWriteFontFace.GetMetrics
title: IDWriteFontFace::GetMetrics
author: windows-sdk-content
description: Obtains design units and common metrics for the font face. These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.
old-location: directwrite\IDWriteFontFace_GetMetrics.htm
tech.root: DirectWrite
ms.assetid: 09271b06-71cb-4702-861f-c3f6b9069c15
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetMetrics, GetMetrics method [Direct Write], GetMetrics method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetMetrics method, IDWriteFontFace.GetMetrics, IDWriteFontFace::GetMetrics, directwrite.IDWriteFontFace_GetMetrics, dwrite/IDWriteFontFace::GetMetrics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace.GetMetrics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteFontFace.GetMetrics
: 
---

# IDWriteFontFace::GetMetrics


## -description


 Obtains design units and common metrics for the font face.
     These metrics are applicable to all the glyphs within a font face and are used by applications for layout calculations.


## -parameters




### -param fontFaceMetrics [out]

Type: <b><a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a>*</b>

When this method returns, a <a href="https://msdn.microsoft.com/ffbf987c-145e-4b93-a48f-8948944c6e33">DWRITE_FONT_METRICS</a> structure that holds metrics (such as ascent, descent, or cap height) for the current font face element.
     The metrics returned by this function are in font design units.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>
 

 

