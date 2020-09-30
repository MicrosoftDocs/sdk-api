---
UID: NF:wingdi.GetEnhMetaFilePaletteEntries
title: GetEnhMetaFilePaletteEntries function (wingdi.h)
description: The GetEnhMetaFilePaletteEntries function retrieves optional palette entries from the specified enhanced metafile.
helpviewer_keywords: ["GetEnhMetaFilePaletteEntries","GetEnhMetaFilePaletteEntries function [Windows GDI]","_win32_GetEnhMetaFilePaletteEntries","gdi.getenhmetafilepaletteentries","wingdi/GetEnhMetaFilePaletteEntries"]
old-location: gdi\getenhmetafilepaletteentries.htm
tech.root: gdi
ms.assetid: 2d61fd6a-cebd-457e-ad00-d3e8bd15584a
ms.date: 12/05/2018
ms.keywords: GetEnhMetaFilePaletteEntries, GetEnhMetaFilePaletteEntries function [Windows GDI], _win32_GetEnhMetaFilePaletteEntries, gdi.getenhmetafilepaletteentries, wingdi/GetEnhMetaFilePaletteEntries
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetEnhMetaFilePaletteEntries
 - wingdi/GetEnhMetaFilePaletteEntries
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Metafile-L1-1-2.dll
 - GDI32Full.dll
api_name:
 - GetEnhMetaFilePaletteEntries
---

# GetEnhMetaFilePaletteEntries function


## -description

The <b>GetEnhMetaFilePaletteEntries</b> function retrieves optional palette entries from the specified enhanced metafile.

## -parameters

### -param hemf [in]

A handle to the enhanced metafile.

### -param nNumEntries [in]

The number of entries to be retrieved from the optional palette.

### -param lpPaletteEntries [out]

A pointer to an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures that receives the palette colors. The array must contain at least as many structures as there are entries specified by the <i>cEntries</i> parameter.

## -returns

If the array pointer is <b>NULL</b> and the enhanced metafile contains an optional palette, the return value is the number of entries in the enhanced metafile's palette; if the array pointer is a valid pointer and the enhanced metafile contains an optional palette, the return value is the number of entries copied; if the metafile does not contain an optional palette, the return value is zero. Otherwise, the return value is GDI_ERROR.

## -remarks

An application can store an optional palette in an enhanced metafile by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setpaletteentries">SetPaletteEntries</a> functions before creating the picture and storing it in the metafile. By doing this, the application can achieve consistent colors when the picture is displayed on a variety of devices.

An application that displays a picture stored in an enhanced metafile can call the <b>GetEnhMetaFilePaletteEntries</b> function to determine whether the optional palette exists. If it does, the application can call the <b>GetEnhMetaFilePaletteEntries</b> function a second time to retrieve the palette entries and then create a logical palette (by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a> function), select it into its device context (by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a> function), and then realize it (by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a> function). After the logical palette has been realized, calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a> function displays the picture using its original colors.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a>