---
UID: NE:dwrite_1.DWRITE_OUTLINE_THRESHOLD
title: DWRITE_OUTLINE_THRESHOLD (dwrite_1.h)
description: The DWRITE_OUTLINE_THRESHOLD enumeration contains values that specify the policy used by the IDWriteFontFace1::GetRecommendedRenderingMode method to determine whether to render glyphs in outline mode.
helpviewer_keywords: ["DWRITE_OUTLINE_THRESHOLD","DWRITE_OUTLINE_THRESHOLD enumeration [Direct Write]","DWRITE_OUTLINE_THRESHOLD_ALIASED","DWRITE_OUTLINE_THRESHOLD_ANTIALIASED","directwrite.dwrite_outline_threshold","dwrite_1/DWRITE_OUTLINE_THRESHOLD","dwrite_1/DWRITE_OUTLINE_THRESHOLD_ALIASED","dwrite_1/DWRITE_OUTLINE_THRESHOLD_ANTIALIASED"]
old-location: directwrite\dwrite_outline_threshold.htm
tech.root: DirectWrite
ms.assetid: F0159E05-A47F-444E-BB07-99AA97DAC0A3
ms.date: 12/05/2018
ms.keywords: DWRITE_OUTLINE_THRESHOLD, DWRITE_OUTLINE_THRESHOLD enumeration [Direct Write], DWRITE_OUTLINE_THRESHOLD_ALIASED, DWRITE_OUTLINE_THRESHOLD_ANTIALIASED, directwrite.dwrite_outline_threshold, dwrite_1/DWRITE_OUTLINE_THRESHOLD, dwrite_1/DWRITE_OUTLINE_THRESHOLD_ALIASED, dwrite_1/DWRITE_OUTLINE_THRESHOLD_ANTIALIASED
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
 - DWRITE_OUTLINE_THRESHOLD
 - dwrite_1/DWRITE_OUTLINE_THRESHOLD
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
 - DWRITE_OUTLINE_THRESHOLD
---

# DWRITE_OUTLINE_THRESHOLD enumeration


## -description

The <b>DWRITE_OUTLINE_THRESHOLD</b> enumeration contains values that specify the policy used by the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode">IDWriteFontFace1::GetRecommendedRenderingMode</a> method to determine whether to render glyphs in outline mode.

## -enum-fields

### -field DWRITE_OUTLINE_THRESHOLD_ANTIALIASED

Graphics system renders anti-aliased outlines.

### -field DWRITE_OUTLINE_THRESHOLD_ALIASED

Graphics system renders aliased outlines.

## -remarks

Glyphs are rendered in outline mode by default at large sizes for performance reasons, but how large (that is, the outline threshold) depends on the quality of outline rendering. If the graphics system renders anti-aliased outlines, a relatively low threshold is used. But if the graphics system renders aliased outlines, a much higher threshold is used.

## -see-also

<a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getrecommendedrenderingmode">IDWriteFontFace1::GetRecommendedRenderingMode</a>

