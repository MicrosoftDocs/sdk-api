---
UID: NF:dwrite_1.IDWriteFontFace1.GetVerticalGlyphVariants
title: IDWriteFontFace1::GetVerticalGlyphVariants
author: windows-sdk-content
description: Retrieves the vertical forms of the nominal glyphs retrieved from GetGlyphIndices.
old-location: directwrite\idwritefontface1_getverticalglyphvariants.htm
tech.root: DirectWrite
ms.assetid: 91CD924E-A664-45C6-B787-61129C31501B
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetVerticalGlyphVariants, GetVerticalGlyphVariants method [Direct Write], GetVerticalGlyphVariants method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetVerticalGlyphVariants method, IDWriteFontFace1.GetVerticalGlyphVariants, IDWriteFontFace1::GetVerticalGlyphVariants, directwrite.idwritefontface1_getverticalglyphvariants, dwrite_1/IDWriteFontFace1::GetVerticalGlyphVariants
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
 - IDWriteFontFace1.GetVerticalGlyphVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_1.h
: 
- IDWriteFontFace1.GetVerticalGlyphVariants
: 
---

# IDWriteFontFace1::GetVerticalGlyphVariants


## -description


Retrieves the vertical forms of the nominal glyphs retrieved from
    GetGlyphIndices.


## -parameters




### -param glyphCount

Type: <b>UINT32</b>

The number of glyphs to retrieve.


### -param nominalGlyphIndices [in]

Type: <b>const UINT16*</b>

Original glyph indices from cmap.


### -param verticalGlyphIndices [out]

Type: <b>UINT16*</b>

The vertical form of glyph indices.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The retrieval uses the font's 'vert' table. This is used in
    CJK vertical layout so the correct characters are shown.

Call <a href="https://msdn.microsoft.com/2dbaec8c-464e-45a5-b420-fa1ec3d224bd">GetGlyphIndices</a> to get the nominal glyph indices, followed by
    calling this to remap the to the substituted forms, when the run
    is sideways, and the font has vertical glyph variants. See <a href="https://msdn.microsoft.com/694F003E-4189-4DC6-ADC8-B94EE8C624BE">HasVerticalGlyphVariants</a> for more info.





## -see-also




<a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace1</a>
 

 

