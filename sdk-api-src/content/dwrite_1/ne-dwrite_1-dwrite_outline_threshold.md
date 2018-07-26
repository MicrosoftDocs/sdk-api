---
UID: NE:dwrite_1.DWRITE_OUTLINE_THRESHOLD
title: DWRITE_OUTLINE_THRESHOLD
author: windows-sdk-content
description: The DWRITE_OUTLINE_THRESHOLD enumeration contains values that specify the policy used by the IDWriteFontFace1::GetRecommendedRenderingMode method to determine whether to render glyphs in outline mode.
old-location: directwrite\dwrite_outline_threshold.htm
old-project: DirectWrite
ms.assetid: F0159E05-A47F-444E-BB07-99AA97DAC0A3
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: DWRITE_OUTLINE_THRESHOLD, DWRITE_OUTLINE_THRESHOLD enumeration [Direct Write], DWRITE_OUTLINE_THRESHOLD_ALIASED, DWRITE_OUTLINE_THRESHOLD_ANTIALIASED, directwrite.dwrite_outline_threshold, dwrite_1/DWRITE_OUTLINE_THRESHOLD, dwrite_1/DWRITE_OUTLINE_THRESHOLD_ALIASED, dwrite_1/DWRITE_OUTLINE_THRESHOLD_ANTIALIASED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_OUTLINE_THRESHOLD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_OUTLINE_THRESHOLD enumeration


## -description


The <b>DWRITE_OUTLINE_THRESHOLD</b> enumeration contains values that specify the policy used by the <a href="https://msdn.microsoft.com/54504bcb-b05c-4b63-8704-8d718cf2ee16">IDWriteFontFace1::GetRecommendedRenderingMode</a> method to determine whether to render glyphs in outline mode.


## -enum-fields




### -field DWRITE_OUTLINE_THRESHOLD_ANTIALIASED

Graphics system renders anti-aliased outlines.


### -field DWRITE_OUTLINE_THRESHOLD_ALIASED

Graphics system renders aliased outlines.


## -remarks



Glyphs are rendered in outline mode by default at large sizes for performance reasons, but how large (that is, the outline threshold) depends on the quality of outline rendering. If the graphics system renders anti-aliased outlines, a relatively low threshold is used. But if the graphics system renders aliased outlines, a much higher threshold is used.




## -see-also




<a href="https://msdn.microsoft.com/54504bcb-b05c-4b63-8704-8d718cf2ee16">IDWriteFontFace1::GetRecommendedRenderingMode</a>
 

 

