---
UID: NF:dwrite_1.IDWriteTextAnalyzer1.GetJustificationOpportunities
title: IDWriteTextAnalyzer1::GetJustificationOpportunities (dwrite_1.h)
author: windows-sdk-content
description: Retrieves justification opportunity information for each of the glyphs given the text and shaping glyph properties.
old-location: directwrite\idwritetextanalyzer1_getjustificationopportunities.htm
tech.root: DirectWrite
ms.assetid: 85D3841F-FA2B-4636-B786-DCD68C72209A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetJustificationOpportunities, GetJustificationOpportunities method [Direct Write], GetJustificationOpportunities method [Direct Write],IDWriteTextAnalyzer1 interface, IDWriteTextAnalyzer1 interface [Direct Write],GetJustificationOpportunities method, IDWriteTextAnalyzer1.GetJustificationOpportunities, IDWriteTextAnalyzer1::GetJustificationOpportunities, directwrite.idwritetextanalyzer1_getjustificationopportunities, dwrite_1/IDWriteTextAnalyzer1::GetJustificationOpportunities
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
 - IDWriteTextAnalyzer1.GetJustificationOpportunities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer1::GetJustificationOpportunities


## -description


Retrieves justification opportunity information for each of the glyphs
    given the text and shaping glyph properties.


## -parameters




### -param fontFace

Type: <b><a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace</a>*</b>

Font face that was used for shaping. This is
    mainly important for returning correct results of the kashida
    width. 

May be NULL. 


### -param fontEmSize

Type: <b>FLOAT</b>

Font em size used for the glyph run.


### -param scriptAnalysis

Type: <b><a href="https://msdn.microsoft.com/dafda5f6-39aa-4577-9213-898bdeddc7c2">DWRITE_SCRIPT_ANALYSIS</a></b>

Script of the text from the itemizer.


### -param textLength

Type: <b>UINT32</b>

Length of the text.


### -param glyphCount

Type: <b>UINT32</b>

Number of glyphs.


### -param textString [in]

Type: <b>const WCHAR*</b>

Characters used to produce the glyphs.


### -param clusterMap [in]

Type: <b>const UINT16*</b>

Clustermap produced from shaping.


### -param glyphProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/debaa84f-8883-4117-9be0-962857b55020">DWRITE_SHAPING_GLYPH_PROPERTIES</a>*</b>

Glyph properties produced from shaping.


### -param justificationOpportunities [out]

Type: <b><a href="https://msdn.microsoft.com/D7D18462-A0A4-4064-B04D-CA8ACED7E34D">DWRITE_JUSTIFICATION_OPPORTUNITY</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/D7D18462-A0A4-4064-B04D-CA8ACED7E34D">DWRITE_JUSTIFICATION_OPPORTUNITY</a> structure that receives info for the
    allowed justification expansion/compression for each glyph.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is called per-run, after shaping is done via the <a href="https://msdn.microsoft.com/9bc373b6-9161-4ffc-a942-50d97d6509c3">IDWriteTextAnalyzer::GetGlyphs</a> method.
    <div class="alert"><b>Note</b>  this function only supports natural metrics (<a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE_NATURAL</a>).</div>
<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/7F79BA25-5D79-4491-82E3-F9B96DD0C37D">IDWriteTextAnalyzer1</a>
 

 

