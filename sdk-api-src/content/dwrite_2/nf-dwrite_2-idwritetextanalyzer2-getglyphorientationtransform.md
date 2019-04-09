---
UID: NF:dwrite_2.IDWriteTextAnalyzer2.GetGlyphOrientationTransform
title: IDWriteTextAnalyzer2::GetGlyphOrientationTransform (dwrite_2.h)
author: windows-sdk-content
description: Returns 2x3 transform matrix for the respective angle to draw the glyph run.
old-location: directwrite\idwritetextanalyzer2_getglyphorientationtransform.htm
tech.root: DirectWrite
ms.assetid: 4483AB14-3BC6-4980-A455-131BCBEBBFB9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGlyphOrientationTransform, GetGlyphOrientationTransform method [Direct Write], GetGlyphOrientationTransform method [Direct Write],IDWriteTextAnalyzer2 interface, IDWriteTextAnalyzer2 interface [Direct Write],GetGlyphOrientationTransform method, IDWriteTextAnalyzer2.GetGlyphOrientationTransform, IDWriteTextAnalyzer2::GetGlyphOrientationTransform, directwrite.idwritetextanalyzer2_getglyphorientationtransform, dwrite_2/IDWriteTextAnalyzer2::GetGlyphOrientationTransform
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextAnalyzer2.GetGlyphOrientationTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalyzer2::GetGlyphOrientationTransform


## -description


Returns 2x3 transform matrix for the respective angle to draw the
    glyph run.

Extends <a href="https://msdn.microsoft.com/583AFE54-F816-4098-844B-C3F838BE46B0">IDWriteTextAnalyzer1::GetGlyphOrientationTransform</a> to pass valid values for the baseline origin rather than zeroes.


## -parameters




### -param glyphOrientationAngle

Type: <b><a href="https://msdn.microsoft.com/BD9D0C11-B286-4E4A-B641-1DB9F75803B0">DWRITE_GLYPH_ORIENTATION_ANGLE</a></b>

A <a href="https://msdn.microsoft.com/BD9D0C11-B286-4E4A-B641-1DB9F75803B0">DWRITE_GLYPH_ORIENTATION_ANGLE</a>-typed value that specifies the angle that was reported into
    <a href="https://msdn.microsoft.com/81BD4C36-273B-4C28-A89E-88BABCAD511A">IDWriteTextAnalysisSink1::SetGlyphOrientation</a>.


### -param isSideways

Type: <b>BOOL</b>

Whether the run's glyphs are sideways or not.


### -param originX

Type: <b>FLOAT</b>

The X value of the baseline origin.


### -param originY

Type: <b>FLOAT</b>

The Y value of the baseline origin.


### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

Returned transform.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62DF6E71-F99D-47E9-A9BE-2A481A60AEDD">IDWriteTextAnalyzer2</a>
 

 

