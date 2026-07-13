---
UID: NE:gdiplusenums.EmfToWmfBitsFlags
title: EmfToWmfBitsFlags (gdiplusenums.h)
description: Specifies options for the Metafile::EmfToWmfBits method, which converts an Enhanced Metafile (EMF) metafile to a Windows Metafile Format (WMF) metafile.
helpviewer_keywords: ["EmfToWmfBitsFlags","EmfToWmfBitsFlags enumeration [GDI+]","EmfToWmfBitsFlagsDefault","EmfToWmfBitsFlagsEmbedEmf","EmfToWmfBitsFlagsIncludePlaceable","EmfToWmfBitsFlagsNoXORClip","_gdiplus_ENUM_EmfToWmfBitsFlags","gdiplus._gdiplus_ENUM_EmfToWmfBitsFlags","gdiplusenums/EmfToWmfBitsFlags","gdiplusenums/EmfToWmfBitsFlagsDefault","gdiplusenums/EmfToWmfBitsFlagsEmbedEmf","gdiplusenums/EmfToWmfBitsFlagsIncludePlaceable","gdiplusenums/EmfToWmfBitsFlagsNoXORClip"]
old-location: gdiplus\_gdiplus_ENUM_EmfToWmfBitsFlags.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\emftowmfbitsflags.htm
ms.date: 12/05/2018
ms.keywords: EmfToWmfBitsFlags, EmfToWmfBitsFlags enumeration [GDI+], EmfToWmfBitsFlagsDefault, EmfToWmfBitsFlagsEmbedEmf, EmfToWmfBitsFlagsIncludePlaceable, EmfToWmfBitsFlagsNoXORClip, _gdiplus_ENUM_EmfToWmfBitsFlags, gdiplus._gdiplus_ENUM_EmfToWmfBitsFlags, gdiplusenums/EmfToWmfBitsFlags, gdiplusenums/EmfToWmfBitsFlagsDefault, gdiplusenums/EmfToWmfBitsFlagsEmbedEmf, gdiplusenums/EmfToWmfBitsFlagsIncludePlaceable, gdiplusenums/EmfToWmfBitsFlagsNoXORClip
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - EmfToWmfBitsFlags
 - gdiplusenums/EmfToWmfBitsFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - EmfToWmfBitsFlags
---

# EmfToWmfBitsFlags enumeration


## -description

Specifies options for the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits">Metafile::EmfToWmfBits</a> method, which converts an Enhanced Metafile (EMF) metafile to a Windows Metafile Format (WMF) metafile.

## -enum-fields

### -field EmfToWmfBitsFlagsDefault:0x00000000

Specifies the default conversion.

### -field EmfToWmfBitsFlagsEmbedEmf:0x00000001

Specifies that the source EMF metafile is embedded as a comment in the resulting WMF metafile.

### -field EmfToWmfBitsFlagsIncludePlaceable:0x00000002

Specifies that the resulting WMF metafile is in the placeable metafile format; that is, it has the additional 22-byte header required by a placeable metafile.

### -field EmfToWmfBitsFlagsNoXORClip:0x00000004

Specifies that the clipping region is stored in the metafile in the traditional way. If you do not set this flag, the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits">Metafile::EmfToWmfBits</a> method applies an optimization that stores the clipping region as a path and simulates clipping by using the XOR operator.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits">Metafile::EmfToWmfBits</a>
