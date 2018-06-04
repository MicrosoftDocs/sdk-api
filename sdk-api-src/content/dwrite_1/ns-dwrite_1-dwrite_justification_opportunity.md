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
 

 

