---
UID: NF:dwrite_3.IDWriteFontFace4.GetGlyphImageData
title: IDWriteFontFace4::GetGlyphImageData
author: windows-sdk-content
description: Gets a pointer to the glyph data based on the desired image format.
old-location: directwrite\idwritefontface4_getglyphimagedata.htm
tech.root: DirectWrite
ms.assetid: 2517A029-5ACF-4CB2-8A20-98253946DF5E
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetGlyphImageData, GetGlyphImageData method [Direct Write], GetGlyphImageData method [Direct Write],IDWriteFontFace4 interface, IDWriteFontFace4 interface [Direct Write],GetGlyphImageData method, IDWriteFontFace4.GetGlyphImageData, IDWriteFontFace4::GetGlyphImageData, directwrite.idwritefontface4_getglyphimagedata, dwrite_3/IDWriteFontFace4::GetGlyphImageData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontFace4.GetGlyphImageData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_3.h
: 
- IDWriteFontFace4.GetGlyphImageData
: 
---

# IDWriteFontFace4::GetGlyphImageData


## -description


Gets a pointer to the glyph data based on the desired image format.


## -parameters




### -param glyphId [in]

Type: <b>UINT16</b>

The ID of the glyph to retrieve image data for.


### -param pixelsPerEm

Type: <b>UINT32</b>

Requested pixels per em.


### -param glyphImageFormat

Type: <b><a href="https://msdn.microsoft.com/ECC868B5-3D17-4D55-8E00-AB446C1C22FE">DWRITE_GLYPH_IMAGE_FORMATS</a></b>

Specifies which formats are supported in the font.


### -param glyphData [out]

Type: <b><a href="https://msdn.microsoft.com/4BBA8B7A-E2DA-445B-AE56-FFA7629E3D06">DWRITE_GLYPH_IMAGE_DATA</a>*</b>

On return contains data for a glyph.


### -param glyphDataContext [out]

Type: <b>void**</b>


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.




## -remarks



The glyphDataContext must be released via <a href="https://msdn.microsoft.com/2A3211C1-90EB-42AE-BCE7-BDDA1D1E6312">ReleaseGlyphImageData</a> when done if the data is not empty,
     similar to <a href="https://msdn.microsoft.com/b5bf3300-cfa0-43db-b513-6c0d695c564e">IDWriteFontFileStream::ReadFileFragment</a> 
       and <a href="https://msdn.microsoft.com/8a12c28e-5595-4255-8fdd-5d546ceed90b">IDWriteFontFileStream::ReleaseFileFragment</a>.
     The data pointer is valid so long as the <a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a> exists and <b>ReleaseGlyphImageData</b> has not
     been called.
     

The <a href="https://msdn.microsoft.com/4BBA8B7A-E2DA-445B-AE56-FFA7629E3D06">DWRITE_GLYPH_IMAGE_DATA::uniqueDataId</a> is valuable for caching purposes so that if the same
     resource is returned more than once, an existing resource can be quickly retrieved rather than
     needing to reparse or decompress the data.
     

The function only returns SVG or raster data - requesting TrueType/CFF/COLR data returns
     DWRITE_E_INVALIDARG. Those must be drawn via DrawGlyphRun or queried using GetGlyphOutline instead.
     Exactly one format may be requested or else the function returns DWRITE_E_INVALIDARG.
     If the glyph does not have that format, the call is not an error, but the function returns empty data. 
     




## -see-also




<a href="https://msdn.microsoft.com/08A0E6F3-611B-4C19-835B-1353D4938181">IDWriteFontFace4</a>
 

 

