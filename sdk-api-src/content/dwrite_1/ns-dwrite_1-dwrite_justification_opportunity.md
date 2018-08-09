---
UID: NS:dwrite_1.DWRITE_JUSTIFICATION_OPPORTUNITY
title: DWRITE_JUSTIFICATION_OPPORTUNITY
author: windows-sdk-content
description: The DWRITE_JUSTIFICATION_OPPORTUNITY structure specifies justification info per glyph.
old-location: directwrite\dwrite_justification_opportunity.htm
old-project: DirectWrite
ms.assetid: D7D18462-A0A4-4064-B04D-CA8ACED7E34D
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: DWRITE_JUSTIFICATION_OPPORTUNITY, DWRITE_JUSTIFICATION_OPPORTUNITY structure [Direct Write], directwrite.dwrite_justification_opportunity, dwrite_1/DWRITE_JUSTIFICATION_OPPORTUNITY
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_JUSTIFICATION_OPPORTUNITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_JUSTIFICATION_OPPORTUNITY structure


## -description


The <b>DWRITE_JUSTIFICATION_OPPORTUNITY</b> structure specifies justification info per glyph.


## -struct-fields




### -field expansionMinimum

Minimum amount of expansion to apply to the side of the glyph. This might vary from zero to infinity, typically being zero except for kashida.


### -field expansionMaximum

Maximum amount of expansion to apply to the side of the glyph. This might vary from zero to infinity, being zero for fixed-size characters and connected scripts, and non-zero for discrete scripts, and non-zero for cursive scripts at expansion points.


### -field compressionMaximum

Maximum amount of compression to apply to the side of the glyph. This might vary from zero up to the glyph cluster size.


### -field expansionPriority

Priority of this expansion point. Larger priorities are applied later, while priority zero does nothing.


### -field compressionPriority

Priority of this compression point. Larger priorities are applied later, while priority zero does nothing.


### -field allowResidualExpansion

Allow this expansion point to use up any remaining slack space even after all expansion priorities have been used up.


### -field allowResidualCompression

Allow this compression point to use up any remaining space even after all compression priorities have been used up.


### -field applyToLeadingEdge

Apply expansion and compression to the leading edge of the glyph. This bit is <b>FALSE</b> (0) for connected scripts, fixed-size characters, and diacritics. It is generally <b>FALSE</b> within a multi-glyph cluster, unless the script allows expansion of glyphs within a cluster, like Thai.


### -field applyToTrailingEdge

Apply expansion and compression to the trailing edge of the glyph. This bit is <b>FALSE</b> (0) for connected scripts, fixed-size characters, and diacritics. It is generally <b>FALSE</b> within a multi-glyph cluster, unless the script allows expansion of glyphs within a cluster, like Thai.


### -field reserved

Reserved


## -see-also




<a href="https://msdn.microsoft.com/85D3841F-FA2B-4636-B786-DCD68C72209A">IDWriteTextAnalyzer1::GetJustificationOpportunities</a>



<a href="https://msdn.microsoft.com/BFBFEA4A-A0D4-4114-B0AB-4338A832ECD4">IDWriteTextAnalyzer1::JustifyGlyphAdvances</a>
 

 

