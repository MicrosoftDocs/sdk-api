---
UID: NS:dwrite_1.DWRITE_CARET_METRICS
title: DWRITE_CARET_METRICS
author: windows-sdk-content
description: The DWRITE_CARET_METRICS structure specifies the metrics for caret placement in a font.
old-location: directwrite\dwrite_caret_metrics.htm
old-project: DirectWrite
ms.assetid: CC7591F8-0671-436F-B0A7-C5D4C183D253
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DWRITE_CARET_METRICS, DWRITE_CARET_METRICS structure [Direct Write], directwrite.dwrite_caret_metrics, dwrite_1/DWRITE_CARET_METRICS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwrite_1.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dwrite_1.h
api_name:
-	DWRITE_CARET_METRICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_CARET_METRICS structure


## -description


The <b>DWRITE_CARET_METRICS</b> structure specifies the metrics for caret placement in a font.


## -struct-fields




### -field slopeRise

Vertical rise of the caret in font design units. Rise / Run yields the caret angle. Rise = 1 for perfectly upright fonts (non-italic).


### -field slopeRun

Horizontal run of the caret in font design units. Rise / Run yields the caret angle. Run = 0 for perfectly upright fonts (non-italic).


### -field offset

Horizontal offset of the caret, in font design units, along the baseline for good appearance. Offset = 0 for perfectly upright fonts (non-italic).


## -see-also




<a href="https://msdn.microsoft.com/D9006617-A5B5-4575-9C00-26F52A73DC0D">IDWriteFontFace1::GetCaretMetrics</a>
 

 

