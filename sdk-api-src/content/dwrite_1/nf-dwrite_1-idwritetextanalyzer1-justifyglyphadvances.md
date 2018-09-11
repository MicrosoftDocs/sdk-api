---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.JustifyGlyphAdvances
title: IDWriteTextAnalyzer1::JustifyGlyphAdvances
author: windows-sdk-content
description: Justifies an array of glyph advances to fit the line width.
old-location: directwrite\idwritetextanalyzer1_justifyglyphadvances.htm
tech.root: DirectWrite
ms.assetid: BFBFEA4A-A0D4-4114-B0AB-4338A832ECD4
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteTextAnalyzer1 interface [Direct Write],JustifyGlyphAdvances method, IDWriteTextAnalyzer1.JustifyGlyphAdvances, IDWriteTextAnalyzer1::JustifyGlyphAdvances, JustifyGlyphAdvances, JustifyGlyphAdvances method [Direct Write], JustifyGlyphAdvances method [Direct Write],IDWriteTextAnalyzer1 interface, directwrite.idwritetextanalyzer1_justifyglyphadvances, dwrite_1/IDWriteTextAnalyzer1::JustifyGlyphAdvances
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteTextAnalyzer1.JustifyGlyphAdvances
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer1::JustifyGlyphAdvances


## -description


Justifies an array of glyph advances to fit the line width.


## -parameters




### -param lineWidth

Type: <b>FLOAT</b>

The line width.


### -param glyphCount

Type: <b>UINT32</b>

The glyph count.


### -param justificationOpportunities [in]

Type: <b>const <a href="https://msdn.microsoft.com/D7D18462-A0A4-4064-B04D-CA8ACED7E34D">DWRITE_JUSTIFICATION_OPPORTUNITY</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/D7D18462-A0A4-4064-B04D-CA8ACED7E34D">DWRITE_JUSTIFICATION_OPPORTUNITY</a> structure that contains info for the
    allowed justification expansion/compression for each glyph. Get this info from <a href="https://msdn.microsoft.com/85D3841F-FA2B-4636-B786-DCD68C72209A">IDWriteTextAnalyzer1::GetJustificationOpportunities</a>. 


### -param glyphAdvances [in]

Type: <b>const FLOAT*</b>

An array of glyph advances.


### -param glyphOffsets [in]

Type: <b>const <a href="https://msdn.microsoft.com/f5a231c0-78df-4fe0-99a8-81fcad517cda">DWRITE_GLYPH_OFFSET</a>*</b>

An array of glyph offsets.


### -param justifiedGlyphAdvances [out]

Type: <b>FLOAT*</b>

The returned array of justified glyph advances.


### -param justifiedGlyphOffsets [out, optional]

Type: <b><a href="https://msdn.microsoft.com/f5a231c0-78df-4fe0-99a8-81fcad517cda">DWRITE_GLYPH_OFFSET</a>*</b>

The returned array of justified glyph offsets.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You call  <b>JustifyGlyphAdvances</b> after you call <a href="https://msdn.microsoft.com/85D3841F-FA2B-4636-B786-DCD68C72209A">IDWriteTextAnalyzer1::GetJustificationOpportunities</a> to collect all the opportunities, and <b>JustifyGlyphAdvances</b>spans across the entire line. The input and output arrays are allowed
    to alias each other, permitting in-place update.




## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>



<a href="https://msdn.microsoft.com/85D3841F-FA2B-4636-B786-DCD68C72209A">IDWriteTextAnalyzer1::GetJustificationOpportunities</a>
 

 

