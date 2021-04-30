---
UID: NE:dwrite_1.DWRITE_BASELINE
title: DWRITE_BASELINE (dwrite_1.h)
description: The DWRITE_BASELINE enumeration contains values that specify the baseline for text alignment.
helpviewer_keywords: ["DWRITE_BASELINE","DWRITE_BASELINE enumeration [Direct Write]","DWRITE_BASELINE_CENTRAL","DWRITE_BASELINE_DEFAULT","DWRITE_BASELINE_HANGING","DWRITE_BASELINE_IDEOGRAPHIC_BOTTOM","DWRITE_BASELINE_IDEOGRAPHIC_TOP","DWRITE_BASELINE_MATH","DWRITE_BASELINE_MAXIMUM","DWRITE_BASELINE_MINIMUM","DWRITE_BASELINE_ROMAN","directwrite.dwrite_baseline","dwrite_1/DWRITE_BASELINE","dwrite_1/DWRITE_BASELINE_CENTRAL","dwrite_1/DWRITE_BASELINE_DEFAULT","dwrite_1/DWRITE_BASELINE_HANGING","dwrite_1/DWRITE_BASELINE_IDEOGRAPHIC_BOTTOM","dwrite_1/DWRITE_BASELINE_IDEOGRAPHIC_TOP","dwrite_1/DWRITE_BASELINE_MATH","dwrite_1/DWRITE_BASELINE_MAXIMUM","dwrite_1/DWRITE_BASELINE_MINIMUM","dwrite_1/DWRITE_BASELINE_ROMAN"]
old-location: directwrite\dwrite_baseline.htm
tech.root: DirectWrite
ms.assetid: A5708481-255B-4777-B689-B61208E3910E
ms.date: 12/05/2018
ms.keywords: DWRITE_BASELINE, DWRITE_BASELINE enumeration [Direct Write], DWRITE_BASELINE_CENTRAL, DWRITE_BASELINE_DEFAULT, DWRITE_BASELINE_HANGING, DWRITE_BASELINE_IDEOGRAPHIC_BOTTOM, DWRITE_BASELINE_IDEOGRAPHIC_TOP, DWRITE_BASELINE_MATH, DWRITE_BASELINE_MAXIMUM, DWRITE_BASELINE_MINIMUM, DWRITE_BASELINE_ROMAN, directwrite.dwrite_baseline, dwrite_1/DWRITE_BASELINE, dwrite_1/DWRITE_BASELINE_CENTRAL, dwrite_1/DWRITE_BASELINE_DEFAULT, dwrite_1/DWRITE_BASELINE_HANGING, dwrite_1/DWRITE_BASELINE_IDEOGRAPHIC_BOTTOM, dwrite_1/DWRITE_BASELINE_IDEOGRAPHIC_TOP, dwrite_1/DWRITE_BASELINE_MATH, dwrite_1/DWRITE_BASELINE_MAXIMUM, dwrite_1/DWRITE_BASELINE_MINIMUM, dwrite_1/DWRITE_BASELINE_ROMAN
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_BASELINE
 - dwrite_1/DWRITE_BASELINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_BASELINE
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

<a href="/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline">IDWriteTextAnalyzer1::GetBaseline</a>

