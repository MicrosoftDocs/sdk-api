---
UID: NF:wingdi.PlayEnhMetaFile
title: PlayEnhMetaFile function (wingdi.h)
description: The PlayEnhMetaFile function displays the picture stored in the specified enhanced-format metafile.
helpviewer_keywords: ["PlayEnhMetaFile","PlayEnhMetaFile function [Windows GDI]","_win32_PlayEnhMetaFile","gdi.playenhmetafile","wingdi/PlayEnhMetaFile"]
old-location: gdi\playenhmetafile.htm
tech.root: gdi
ms.assetid: 51e8937b-0c42-49fe-8930-7af303fce788
ms.date: 12/05/2018
ms.keywords: PlayEnhMetaFile, PlayEnhMetaFile function [Windows GDI], _win32_PlayEnhMetaFile, gdi.playenhmetafile, wingdi/PlayEnhMetaFile
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
 - PlayEnhMetaFile
 - wingdi/PlayEnhMetaFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - PlayEnhMetaFile
---

# PlayEnhMetaFile function


## -description

The <b>PlayEnhMetaFile</b> function displays the picture stored in the specified enhanced-format metafile.

## -parameters

### -param hdc [in]

A handle to the device context for the output device on which the picture will appear.

### -param hmf [in]

A handle to the enhanced metafile.

### -param lprect [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the coordinates of the bounding rectangle used to display the picture. The coordinates are specified in logical units.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

When an application calls the <b>PlayEnhMetaFile</b> function, the system uses the picture frame in the enhanced-metafile header to map the picture onto the rectangle pointed to by the <i>lpRect</i> parameter. (This picture may be sheared or rotated by setting the world transform in the output device before calling <b>PlayEnhMetaFile</b>.) Points along the edges of the rectangle are included in the picture.

An enhanced-metafile picture can be clipped by defining the clipping region in the output device before playing the enhanced metafile.

If an enhanced metafile contains an optional palette, an application can achieve consistent colors by setting up a color palette on the output device before calling <b>PlayEnhMetaFile</b>. To retrieve the optional palette, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepaletteentries">GetEnhMetaFilePaletteEntries</a> function.

An enhanced metafile can be embedded in a newly created enhanced metafile by calling <b>PlayEnhMetaFile</b> and playing the source enhanced metafile into the device context for the new enhanced metafile.

The states of the output device context are preserved by this function. Any object created but not deleted in the enhanced metafile is deleted by this function.

To stop this function, an application can call the <a href="/windows/desktop/api/wingdi/nf-wingdi-canceldc">CancelDC</a> function from another thread to terminate the operation. In this case, the function returns <b>FALSE</b>.


#### Examples

For an example, see <a href="/windows/desktop/gdi/opening-an-enhanced-metafile-and-displaying-its-contents">Opening an Enhanced Metafile and Displaying Its Contents</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-canceldc">CancelDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafileheader">GetEnhMetaFileHeader</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepaletteentries">GetEnhMetaFilePaletteEntries</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>