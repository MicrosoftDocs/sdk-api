---
UID: NS:wingdi.tagMETAFILEPICT
title: METAFILEPICT (wingdi.h)
description: Defines the metafile picture format used for exchanging metafile data through the clipboard.
helpviewer_keywords: ["*LPMETAFILEPICT","LPMETAFILEPICT","LPMETAFILEPICT structure pointer [Data Exchange]","METAFILEPICT","METAFILEPICT structure [Data Exchange]","_win32_METAFILEPICT_str","_win32_metafilepict_str_cpp","dataxchg.metafilepict","wingdi/LPMETAFILEPICT","wingdi/METAFILEPICT","winui._win32_metafilepict_str"]
old-location: dataxchg\metafilepict.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\clipboard\clipboardreference\clipboardstructures\metafilepict.htm
ms.date: 12/05/2018
ms.keywords: '*LPMETAFILEPICT, LPMETAFILEPICT, LPMETAFILEPICT structure pointer [Data Exchange], METAFILEPICT, METAFILEPICT structure [Data Exchange], _win32_METAFILEPICT_str, _win32_metafilepict_str_cpp, dataxchg.metafilepict, wingdi/LPMETAFILEPICT, wingdi/METAFILEPICT, winui._win32_metafilepict_str'
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
req.typenames: METAFILEPICT, *LPMETAFILEPICT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMETAFILEPICT
 - wingdi/tagMETAFILEPICT
 - LPMETAFILEPICT
 - wingdi/LPMETAFILEPICT
 - METAFILEPICT
 - wingdi/METAFILEPICT
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
 - METAFILEPICT
---

# METAFILEPICT structure


## -description

Defines the metafile picture format used for exchanging metafile data through the clipboard.

## -struct-fields

### -field mm

Type: <b>LONG</b>

The mapping mode in which the picture is drawn.

### -field xExt

Type: <b>LONG</b>

The size of the metafile picture for all modes except the <b>MM_ISOTROPIC</b> and <b>MM_ANISOTROPIC</b> modes. (For more information about these modes, see the <b>yExt</b> member.) The x-extent specifies the width of the rectangle within which the picture is drawn. The coordinates are in units that correspond to the mapping mode.

### -field yExt

Type: <b>LONG</b>

The size of the metafile picture for all modes except the <b>MM_ISOTROPIC</b> and <b>MM_ANISOTROPIC</b> modes. The y-extent specifies the height of the rectangle within which the picture is drawn. The coordinates are in units that correspond to the mapping mode. For <b>MM_ISOTROPIC</b> and <b>MM_ANISOTROPIC</b> modes, which can be scaled, the <b>xExt</b> and <b>yExt</b> members contain an optional suggested size in <b>MM_HIMETRIC</b> units. For <b>MM_ANISOTROPIC</b> pictures, <b>xExt</b> and <b>yExt</b> can be zero when no suggested size is supplied. For <b>MM_ISOTROPIC</b> pictures, an aspect ratio must be supplied even when no suggested size is given. (If a suggested size is given, the aspect ratio is implied by the size.) To give an aspect ratio without implying a suggested size, set <b>xExt</b> and <b>yExt</b> to negative values whose ratio is the appropriate aspect ratio. The magnitude of the negative <b>xExt</b> and <b>yExt</b> values is ignored; only the ratio is used.

### -field hMF

Type: <b>HMETAFILE</b>

A handle to a memory metafile.

## -see-also

<a href="/windows/desktop/dataxchg/clipboard">Clipboard</a>



<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setclipboarddata">SetClipboardData</a>