---
UID: NF:d2d1_3.ID2D1Device4.SetMaximumColorGlyphCacheMemory
title: ID2D1Device4::SetMaximumColorGlyphCacheMemory (d2d1_3.h)
description: Sets the maximum capacity of the color glyph cache.
helpviewer_keywords: ["ID2D1Device4 interface [Direct2D]","SetMaximumColorGlyphCacheMemory method","ID2D1Device4.SetMaximumColorGlyphCacheMemory","ID2D1Device4::SetMaximumColorGlyphCacheMemory","SetMaximumColorGlyphCacheMemory","SetMaximumColorGlyphCacheMemory method [Direct2D]","SetMaximumColorGlyphCacheMemory method [Direct2D]","ID2D1Device4 interface","d2d1_3/ID2D1Device4::SetMaximumColorGlyphCacheMemory","direct2d.id2d1device4_setmaximumcolorglyphcachememory"]
old-location: direct2d\id2d1device4_setmaximumcolorglyphcachememory.htm
tech.root: Direct2D
ms.assetid: 477386A0-0EED-489A-BBFD-8371153D5BA1
ms.date: 12/05/2018
ms.keywords: ID2D1Device4 interface [Direct2D],SetMaximumColorGlyphCacheMemory method, ID2D1Device4.SetMaximumColorGlyphCacheMemory, ID2D1Device4::SetMaximumColorGlyphCacheMemory, SetMaximumColorGlyphCacheMemory, SetMaximumColorGlyphCacheMemory method [Direct2D], SetMaximumColorGlyphCacheMemory method [Direct2D],ID2D1Device4 interface, d2d1_3/ID2D1Device4::SetMaximumColorGlyphCacheMemory, direct2d.id2d1device4_setmaximumcolorglyphcachememory
req.header: d2d1_3.h
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Device4::SetMaximumColorGlyphCacheMemory
 - d2d1_3/ID2D1Device4::SetMaximumColorGlyphCacheMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device4.SetMaximumColorGlyphCacheMemory
---

# ID2D1Device4::SetMaximumColorGlyphCacheMemory


## -description

Sets the maximum capacity of the color glyph cache.

## -parameters

### -param maximumInBytes

Type: <b>UINT64</b>

The maximum capacity of the color glyph cache.

## -remarks

The color glyph cache is used to store color bitmap glyphs and SVG glyphs, enabling faster performance if the same
      glyphs are needed again. The capacity determines the amount of memory that D2D may use to store glyphs that the application does not already reference. If the
      application references a glyph using <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-getcolorbitmapglyphimage">GetColorBitmapGlyphImage</a> or
      <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-getsvgglyphimage">GetSvgGlyphImage</a>, after it has been evicted, this
      glyph does not count toward the cache capacity.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device4">ID2D1Device4</a>