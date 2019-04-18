---
UID: NF:dwrite_1.IDWriteTextAnalysisSource1.GetVerticalGlyphOrientation
title: IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation (dwrite_1.h)
author: windows-sdk-content
description: Used by the text analyzer to obtain the desired glyph orientation and resolved bidi level.
old-location: directwrite\idwritetextanalysissource1_getverticalglyphorientation.htm
tech.root: DirectWrite
ms.assetid: 2F229E8A-171D-4DED-9E9E-F2925855E8C0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVerticalGlyphOrientation, GetVerticalGlyphOrientation method [Direct Write], GetVerticalGlyphOrientation method [Direct Write],IDWriteTextAnalysisSource1 interface, IDWriteTextAnalysisSource1 interface [Direct Write],GetVerticalGlyphOrientation method, IDWriteTextAnalysisSource1.GetVerticalGlyphOrientation, IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation, directwrite.idwritetextanalysissource1_getverticalglyphorientation, dwrite_1/IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation
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
 - IDWriteTextAnalysisSource1.GetVerticalGlyphOrientation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextAnalysisSource1::GetVerticalGlyphOrientation


## -description


Used by the text analyzer to obtain the desired glyph
    orientation and resolved bidi level.


## -parameters




### -param textPosition

Type: <b>UINT32</b>

The text position.


### -param textLength [out]

Type: <b>UINT32*</b>

A pointer to the text length.


### -param glyphOrientation [out]

Type: <b><a href="https://msdn.microsoft.com/F13CD254-0D6A-4549-A2C2-3D3126E7B2EB">DWRITE_VERTICAL_GLYPH_ORIENTATION</a>*</b>

A <a href="https://msdn.microsoft.com/F13CD254-0D6A-4549-A2C2-3D3126E7B2EB">DWRITE_VERTICAL_GLYPH_ORIENTATION</a>-typed value that specifies the desired kind of glyph orientation for the text.


### -param bidiLevel [out]

Type: <b>UINT8*</b>

A pointer to the resolved bidi level.


## -returns



Type: <b>HRESULT</b>

Returning an error will abort the
    analysis.




## -remarks



The text analyzer calls back to this to get the desired glyph
    orientation and resolved bidi level, which it uses along with the
    script properties of the text to determine the actual orientation of
    each character, which it reports back to the client via the sink
    SetGlyphOrientation method.




## -see-also




<a href="https://msdn.microsoft.com/CFB9DB16-1F0B-409F-97BC-BB4B693AB3D6">IDWriteTextAnalysisSource1</a>
 

 

