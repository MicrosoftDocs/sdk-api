---
UID: NF:d2d1_3.ID2D1Device4.SetMaximumColorGlyphCacheMemory
title: ID2D1Device4::SetMaximumColorGlyphCacheMemory
author: windows-sdk-content
description: Sets the maximum capacity of the color glyph cache.
old-location: direct2d\id2d1device4_setmaximumcolorglyphcachememory.htm
tech.root: direct2d
ms.assetid: 477386A0-0EED-489A-BBFD-8371153D5BA1
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: ID2D1Device4 interface [Direct2D],SetMaximumColorGlyphCacheMemory method, ID2D1Device4.SetMaximumColorGlyphCacheMemory, ID2D1Device4::SetMaximumColorGlyphCacheMemory, SetMaximumColorGlyphCacheMemory, SetMaximumColorGlyphCacheMemory method [Direct2D], SetMaximumColorGlyphCacheMemory method [Direct2D],ID2D1Device4 interface, d2d1_3/ID2D1Device4::SetMaximumColorGlyphCacheMemory, direct2d.id2d1device4_setmaximumcolorglyphcachememory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device4.SetMaximumColorGlyphCacheMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device4::SetMaximumColorGlyphCacheMemory


## -description


Sets the maximum capacity of the color glyph cache. 


## -parameters




### -param maximumInBytes

Type: <b>UINT64</b>

The maximum capacity of the color glyph cache.


## -returns



This method does not return a value.




## -remarks



The color glyph cache is used to store color bitmap glyphs and SVG glyphs, enabling faster performance if the same
      glyphs are needed again. The capacity determines the amount of memory that D2D may use to store glyphs that the application does not already reference. If the
      application references a glyph using <a href="https://msdn.microsoft.com/493224CD-A31E-405B-A084-24C377F713A0">GetColorBitmapGlyphImage</a> or
      <a href="https://msdn.microsoft.com/096ED0A3-6222-4DC4-9463-E90D36F2442A">GetSvgGlyphImage</a>, after it has been evicted, this
      glyph does not count toward the cache capacity.




## -see-also




<a href="https://msdn.microsoft.com/B91E4E63-5FB5-4470-A3B9-F94008EAE4E9">ID2D1Device4</a>
 

 

