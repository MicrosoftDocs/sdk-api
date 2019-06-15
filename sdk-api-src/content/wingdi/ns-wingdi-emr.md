---
UID: NS:wingdi.tagEMR
title: EMR (wingdi.h)
author: windows-sdk-content
description: The EMR structure provides the base structure for all enhanced metafile records. An enhanced metafile record contains the parameters for a specific GDI function used to create part of a picture in an enhanced format metafile.
old-location: gdi\emr.htm
tech.root: gdi
ms.assetid: 06582047-b64b-44ec-ae27-1f8ed7c56b97
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEMR, EMR, EMR structure [Windows GDI], PEMR, PEMR structure pointer [Windows GDI], _win32_EMR_str, gdi.emr, wingdi/EMR, wingdi/PEMR"
ms.topic: struct
f1_keywords: ["wingdi/EMR"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMR
product: Windows
targetos: Windows
req.typenames: EMR, *PEMR
req.redist: 
ms.custom: 19H1
---

# EMR structure


## -description



The <b>EMR</b> structure provides the base structure for all enhanced metafile records. An enhanced metafile record contains the parameters for a specific GDI function used to create part of a picture in an enhanced format metafile.




## -struct-fields




### -field iType

The record type. The parameter can be one of the following (with a link to the associated record structure).

<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_ABORTPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemralphablend">EMR_ALPHABLEND</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemranglearc">EMR_ANGLEARC</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrarc">EMR_ARC</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrarc">EMR_ARCTO</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_BEGINPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrbitblt">EMR_BITBLT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrarc">EMR_CHORD</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_CLOSEFIGURE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagcolorcorrectpalette">EMR_COLORCORRECTPALETTE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagcolormatchtotarget">EMR_COLORMATCHTOTARGETW</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrcreatebrushindirect">EMR_CREATEBRUSHINDIRECT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrcreatecolorspace">EMR_CREATECOLORSPACE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrcreatecolorspacew">EMR_CREATECOLORSPACEW</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrcreatedibpatternbrushpt">EMR_CREATEDIBPATTERNBRUSHPT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrcreatemonobrush">EMR_CREATEMONOBRUSH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrcreatepalette">EMR_CREATEPALETTE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrcreatepen">EMR_CREATEPEN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetcolorspace">EMR_DELETECOLORSPACE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectobject">EMR_DELETEOBJECT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrellipse">EMR_ELLIPSE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_ENDPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemreof">EMR_EOF</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrexcludecliprect">EMR_EXCLUDECLIPRECT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrextcreatefontindirectw">EMR_EXTCREATEFONTINDIRECTW</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrextcreatepen">EMR_EXTCREATEPEN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrextfloodfill">EMR_EXTFLOODFILL</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrextselectcliprgn">EMR_EXTSELECTCLIPRGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrexttextouta">EMR_EXTTEXTOUTA</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrexttextouta">EMR_EXTTEXTOUTW</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrfillpath">EMR_FILLPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrfillrgn">EMR_FILLRGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_FLATTENPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrframergn">EMR_FRAMERGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrgdicomment">EMR_GDICOMMENT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrglsboundedrecord">EMR_GLSBOUNDEDRECORD</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrglsrecord">EMR_GLSRECORD</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrgradientfill">EMR_GRADIENTFILL</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrexcludecliprect">EMR_INTERSECTCLIPRECT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrinvertrgn">EMR_INVERTRGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrlineto">EMR_LINETO</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrmaskblt">EMR_MASKBLT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrmodifyworldtransform">EMR_MODIFYWORLDTRANSFORM</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrlineto">EMR_MOVETOEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemroffsetcliprgn">EMR_OFFSETCLIPRGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrinvertrgn">EMR_PAINTRGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrarc">EMR_PIE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpixelformat">EMR_PIXELFORMAT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrplgblt">EMR_PLGBLT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline">EMR_POLYBEZIER</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline16">EMR_POLYBEZIER16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline">EMR_POLYBEZIERTO</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline16">EMR_POLYBEZIERTO16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolydraw">EMR_POLYDRAW</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolydraw16">EMR_POLYDRAW16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline">EMR_POLYGON</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline16">EMR_POLYGON16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline">EMR_POLYLINE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline16">EMR_POLYLINE16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline">EMR_POLYLINETO</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolyline16">EMR_POLYLINETO16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolypolyline">EMR_POLYPOLYGON</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolypolyline16">EMR_POLYPOLYGON16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolypolyline">EMR_POLYPOLYLINE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolypolyline16">EMR_POLYPOLYLINE16</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolytextouta">EMR_POLYTEXTOUTA</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrpolytextouta">EMR_POLYTEXTOUTW</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_REALIZEPALETTE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrellipse">EMR_RECTANGLE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrresizepalette">EMR_RESIZEPALETTE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrrestoredc">EMR_RESTOREDC</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrroundrect">EMR_ROUNDRECT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_SAVEDC</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrscaleviewportextex">EMR_SCALEVIEWPORTEXTEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrscaleviewportextex">EMR_SCALEWINDOWEXTEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SELECTCLIPPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectobject">EMR_SELECTOBJECT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectpalette">EMR_SELECTPALETTE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetarcdirection">EMR_SETARCDIRECTION</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsettextcolor">EMR_SETBKCOLOR</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETBKMODE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetviewportextex">EMR_SETBRUSHORGEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetcoloradjustment">EMR_SETCOLORADJUSTMENT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetcolorspace">EMR_SETCOLORSPACE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetdibitstodevice">EMR_SETDIBITSTODEVICE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETICMMODE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrseticmprofile">EMR_SETICMPROFILEA</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrseticmprofile">EMR_SETICMPROFILEW</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETLAYOUT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETMAPMODE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetmapperflags">EMR_SETMAPPERFLAGS</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_SETMETARGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetmiterlimit">EMR_SETMITERLIMIT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetpaletteentries">EMR_SETPALETTEENTRIES</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetpixelv">EMR_SETPIXELV</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETPOLYFILLMODE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETROP2</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETSTRETCHBLTMODE</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrselectclippath">EMR_SETTEXTALIGN</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsettextcolor">EMR_SETTEXTCOLOR</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetviewportextex">EMR_SETVIEWPORTEXTEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetviewportorgex">EMR_SETVIEWPORTORGEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetviewportextex">EMR_SETWINDOWEXTEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetviewportextex">EMR_SETWINDOWORGEX</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrsetworldtransform">EMR_SETWORLDTRANSFORM</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrstretchblt">EMR_STRETCHBLT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrstretchdibits">EMR_STRETCHDIBITS</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrfillpath">EMR_STROKEANDFILLPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrfillpath">EMR_STROKEPATH</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagemrtransparentblt">EMR_TRANSPARENTBLT</a>
<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-tagabortpath">EMR_WIDENPATH</a>

### -field nSize

The size of the record, in bytes. This member must be a multiple of four.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/metafiles">Metafiles Overview</a>
 

 

