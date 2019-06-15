---
UID: NF:dwrite_1.IDWriteFontFace1.GetDesignGlyphAdvances
title: IDWriteFontFace1::GetDesignGlyphAdvances (dwrite_1.h)
author: windows-sdk-content
description: Retrieves the advances in design units for a sequences of glyphs.
old-location: directwrite\idwritefontface1_getdesignglyphadvances.htm
tech.root: DirectWrite
ms.assetid: 1E40518F-51E0-48F6-99ED-BE9407B61B6E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDesignGlyphAdvances, GetDesignGlyphAdvances method [Direct Write], GetDesignGlyphAdvances method [Direct Write],IDWriteFontFace1 interface, IDWriteFontFace1 interface [Direct Write],GetDesignGlyphAdvances method, IDWriteFontFace1.GetDesignGlyphAdvances, IDWriteFontFace1::GetDesignGlyphAdvances, directwrite.idwritefontface1_getdesignglyphadvances, dwrite_1/IDWriteFontFace1::GetDesignGlyphAdvances
ms.topic: method
f1_keywords: ["dwrite_1/IDWriteFontFace1.GetDesignGlyphAdvances"]
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
 - IDWriteFontFace1.GetDesignGlyphAdvances
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFace1::GetDesignGlyphAdvances


## -description


Retrieves the advances in design units for a sequences of glyphs.


## -parameters




### -param glyphCount

Type: <b>UINT32</b>

The number of glyphs to retrieve advances for.


### -param glyphIndices [in]

Type: <b>const UINT16*</b>

An array of glyph id's to retrieve advances for.


### -param glyphAdvances [out]

Type: <b>INT32*</b>

The returned advances in font design units for
    each glyph.


### -param isSideways

Type: <b>BOOL</b>

Retrieve the glyph's vertical advance height
    rather than horizontal advance widths.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is equivalent to calling GetGlyphMetrics and using only the
    advance width and height.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_1/nn-dwrite_1-idwritefontface1">IDWriteFontFace1</a>
 

 

