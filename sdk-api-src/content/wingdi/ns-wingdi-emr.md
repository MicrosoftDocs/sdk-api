---
UID: NS:wingdi.tagEMR
title: EMR (wingdi.h)
description: The EMR structure provides the base structure for all enhanced metafile records. An enhanced metafile record contains the parameters for a specific GDI function used to create part of a picture in an enhanced format metafile.
helpviewer_keywords: ["*PEMR","EMR","EMR structure [Windows GDI]","PEMR","PEMR structure pointer [Windows GDI]","_win32_EMR_str","gdi.emr","wingdi/EMR","wingdi/PEMR"]
old-location: gdi\emr.htm
tech.root: gdi
ms.assetid: 06582047-b64b-44ec-ae27-1f8ed7c56b97
ms.date: 12/05/2018
ms.keywords: '*PEMR, EMR, EMR structure [Windows GDI], PEMR, PEMR structure pointer [Windows GDI], _win32_EMR_str, gdi.emr, wingdi/EMR, wingdi/PEMR'
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
targetos: Windows
req.typenames: EMR, *PEMR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMR
 - wingdi/tagEMR
 - PEMR
 - wingdi/PEMR
 - EMR
 - wingdi/EMR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMR
---

# EMR structure


## -description

The <b>EMR</b> structure provides the base structure for all enhanced metafile records. An enhanced metafile record contains the parameters for a specific GDI function used to create part of a picture in an enhanced format metafile.

## -struct-fields

### -field iType

The record type. The parameter can be one of the following (with a link to the associated record structure).

<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_ABORTPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emralphablend">EMR_ALPHABLEND</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emranglearc">EMR_ANGLEARC</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrarc">EMR_ARC</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrarc">EMR_ARCTO</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_BEGINPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrbitblt">EMR_BITBLT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrarc">EMR_CHORD</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_CLOSEFIGURE</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrcolorcorrectpalette">EMR_COLORCORRECTPALETTE</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrcolormatchtotarget">EMR_COLORMATCHTOTARGETW</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatebrushindirect">EMR_CREATEBRUSHINDIRECT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatecolorspace">EMR_CREATECOLORSPACE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatecolorspacew">EMR_CREATECOLORSPACEW</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatedibpatternbrushpt">EMR_CREATEDIBPATTERNBRUSHPT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatemonobrush">EMR_CREATEMONOBRUSH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatepalette">EMR_CREATEPALETTE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatepen">EMR_CREATEPEN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetcolorspace">EMR_DELETECOLORSPACE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectobject">EMR_DELETEOBJECT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrellipse">EMR_ELLIPSE</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_ENDPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emreof">EMR_EOF</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrexcludecliprect">EMR_EXCLUDECLIPRECT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrextcreatefontindirectw">EMR_EXTCREATEFONTINDIRECTW</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrextcreatepen">EMR_EXTCREATEPEN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrextfloodfill">EMR_EXTFLOODFILL</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrextselectcliprgn">EMR_EXTSELECTCLIPRGN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrexttextouta">EMR_EXTTEXTOUTA</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrexttextouta">EMR_EXTTEXTOUTW</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrfillpath">EMR_FILLPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrfillrgn">EMR_FILLRGN</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_FLATTENPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrframergn">EMR_FRAMERGN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrgdicomment">EMR_GDICOMMENT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrglsboundedrecord">EMR_GLSBOUNDEDRECORD</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrglsrecord">EMR_GLSRECORD</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrgradientfill">EMR_GRADIENTFILL</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrexcludecliprect">EMR_INTERSECTCLIPRECT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrinvertrgn">EMR_INVERTRGN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrlineto">EMR_LINETO</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrmaskblt">EMR_MASKBLT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrmodifyworldtransform">EMR_MODIFYWORLDTRANSFORM</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrlineto">EMR_MOVETOEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emroffsetcliprgn">EMR_OFFSETCLIPRGN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrinvertrgn">EMR_PAINTRGN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrarc">EMR_PIE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpixelformat">EMR_PIXELFORMAT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrplgblt">EMR_PLGBLT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline">EMR_POLYBEZIER</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline16">EMR_POLYBEZIER16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline">EMR_POLYBEZIERTO</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline16">EMR_POLYBEZIERTO16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolydraw">EMR_POLYDRAW</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolydraw16">EMR_POLYDRAW16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline">EMR_POLYGON</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline16">EMR_POLYGON16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline">EMR_POLYLINE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline16">EMR_POLYLINE16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline">EMR_POLYLINETO</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolyline16">EMR_POLYLINETO16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolypolyline">EMR_POLYPOLYGON</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolypolyline16">EMR_POLYPOLYGON16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolypolyline">EMR_POLYPOLYLINE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolypolyline16">EMR_POLYPOLYLINE16</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolytextouta">EMR_POLYTEXTOUTA</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrpolytextouta">EMR_POLYTEXTOUTW</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_REALIZEPALETTE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrellipse">EMR_RECTANGLE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrresizepalette">EMR_RESIZEPALETTE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrrestoredc">EMR_RESTOREDC</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrroundrect">EMR_ROUNDRECT</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_SAVEDC</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrscaleviewportextex">EMR_SCALEVIEWPORTEXTEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrscaleviewportextex">EMR_SCALEWINDOWEXTEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SELECTCLIPPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectobject">EMR_SELECTOBJECT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectpalette">EMR_SELECTPALETTE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetarcdirection">EMR_SETARCDIRECTION</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrsetbkcolor">EMR_SETBKCOLOR</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETBKMODE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetviewportextex">EMR_SETBRUSHORGEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetcoloradjustment">EMR_SETCOLORADJUSTMENT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetcolorspace">EMR_SETCOLORSPACE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetdibitstodevice">EMR_SETDIBITSTODEVICE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETICMMODE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrseticmprofile">EMR_SETICMPROFILEA</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrseticmprofile">EMR_SETICMPROFILEW</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETLAYOUT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETMAPMODE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetmapperflags">EMR_SETMAPPERFLAGS</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_SETMETARGN</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetmiterlimit">EMR_SETMITERLIMIT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetpaletteentries">EMR_SETPALETTEENTRIES</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetpixelv">EMR_SETPIXELV</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETPOLYFILLMODE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETROP2</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETSTRETCHBLTMODE</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrselectclippath">EMR_SETTEXTALIGN</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrsetbkcolor">EMR_SETTEXTCOLOR</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetviewportextex">EMR_SETVIEWPORTEXTEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetviewportorgex">EMR_SETVIEWPORTORGEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetviewportextex">EMR_SETWINDOWEXTEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetviewportextex">EMR_SETWINDOWORGEX</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrsetworldtransform">EMR_SETWORLDTRANSFORM</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrstretchblt">EMR_STRETCHBLT</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrstretchdibits">EMR_STRETCHDIBITS</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrfillpath">EMR_STROKEANDFILLPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrfillpath">EMR_STROKEPATH</a>
<a href="/windows/desktop/api/wingdi/ns-wingdi-emrtransparentblt">EMR_TRANSPARENTBLT</a>
<a href="/windows/win32/api/wingdi/ns-wingdi-emrabortpath">EMR_WIDENPATH</a>

### -field nSize

The size of the record, in bytes. This member must be a multiple of four.

## -see-also

<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>