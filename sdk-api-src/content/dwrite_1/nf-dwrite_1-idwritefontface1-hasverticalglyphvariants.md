---
UID: NF:dwrite_1.IDWriteFontFace1.HasVerticalGlyphVariants
title: IDWriteFontFace1::HasVerticalGlyphVariants (dwrite_1.h)
author: windows-sdk-content
description: Determines whether the font has any vertical glyph variants.
old-location: directwrite\idwritefontface1_hasverticalglyphvariants.htm
tech.root: DirectWrite
ms.assetid: 694F003E-4189-4DC6-ADC8-B94EE8C624BE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HasVerticalGlyphVariants, HasVerticalGlyphVariants method [Direct Write], HasVerticalGlyphVariants method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],HasVerticalGlyphVariants method, IDWriteFontFace1.HasVerticalGlyphVariants, IDWriteFontFace1::HasVerticalGlyphVariants, directwrite.idwritefontface1_hasverticalglyphvariants, dwrite_1/IDWriteFontFace1::HasVerticalGlyphVariants
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
 - IDWriteFontFace1.HasVerticalGlyphVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace1::HasVerticalGlyphVariants


## -description


Determines whether the font has any vertical glyph variants.


## -parameters






## -returns



Returns TRUE if the font contains vertical glyph variants, otherwise FALSE.




## -remarks



For OpenType fonts, <b>HasVerticalGlyphVariants</b> returns TRUE if the font contains a "vert"feature. 


<a href="https://msdn.microsoft.com/91CD924E-A664-45C6-B787-61129C31501B">IDWriteFontFace1::GetVerticalGlyphVariants</a> retrieves the vertical forms of the nominal glyphs that are retrieved from <a href="https://msdn.microsoft.com/2dbaec8c-464e-45a5-b420-fa1ec3d224bd">IDWriteFontFace::GetGlyphIndices</a>. 




## -see-also




<a href="https://msdn.microsoft.com/1DB7156F-0578-46A0-8C96-E1E34FF4E49E">IDWriteFontFace1</a>



<a href="https://msdn.microsoft.com/91CD924E-A664-45C6-B787-61129C31501B">IDWriteFontFace1::GetVerticalGlyphVariants</a>



<a href="https://msdn.microsoft.com/2dbaec8c-464e-45a5-b420-fa1ec3d224bd">IDWriteFontFace::GetGlyphIndices</a>
 

 

