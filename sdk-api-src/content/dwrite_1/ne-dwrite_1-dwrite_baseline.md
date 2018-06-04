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

# DWRITE_BASELINE enumeration


## -description


The <b>DWRITE_BASELINE</b> enumeration contains values that specify the baseline for text alignment.


## -enum-fields




### -field DWRITE_BASELINE_DEFAULT

The Roman baseline for horizontal; the Central baseline for vertical.


### -field DWRITE_BASELINE_ROMAN

The baseline that is used by alphabetic scripts such as Latin, Greek, and Cyrillic.


### -field DWRITE_BASELINE_CENTRAL

Central baseline, which is generally used for vertical text.


### -field DWRITE_BASELINE_MATH

Mathematical baseline, which math characters are centered on.


### -field DWRITE_BASELINE_HANGING

Hanging baseline, which is used in scripts like Devanagari.


### -field DWRITE_BASELINE_IDEOGRAPHIC_BOTTOM

Ideographic bottom baseline for CJK, left in vertical.


### -field DWRITE_BASELINE_IDEOGRAPHIC_TOP

Ideographic top baseline for CJK, right in vertical.


### -field DWRITE_BASELINE_MINIMUM

The bottom-most extent in horizontal, left-most in vertical.


### -field DWRITE_BASELINE_MAXIMUM

The top-most extent in horizontal, right-most in vertical.


## -see-also




<a href="https://msdn.microsoft.com/5ACD5075-BD96-41FC-AE36-8D5D03F2EB54">IDWriteTextAnalyzer1::GetBaseline</a>
 

 

