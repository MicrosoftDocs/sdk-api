---
UID: NS:winuser._ICONINFO
title: ICONINFO (winuser.h)
description: Contains information about an icon or a cursor.
helpviewer_keywords: ["*PICONINFO","ICONINFO","ICONINFO structure [Menus and Other Resources]","PICONINFO","PICONINFO structure pointer [Menus and Other Resources]","_win32_ICONINFO_str","_win32_iconinfo_str_cpp","menurc.iconinfo","winui._win32_iconinfo_str","winuser/ICONINFO","winuser/PICONINFO"]
old-location: menurc\iconinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconstructures\iconinfo.htm
ms.date: 12/05/2018
ms.keywords: '*PICONINFO, ICONINFO, ICONINFO structure [Menus and Other Resources], PICONINFO, PICONINFO structure pointer [Menus and Other Resources], _win32_ICONINFO_str, _win32_iconinfo_str_cpp, menurc.iconinfo, winui._win32_iconinfo_str, winuser/ICONINFO, winuser/PICONINFO'
req.header: winuser.h
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
req.typenames: ICONINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ICONINFO
 - winuser/_ICONINFO
 - ICONINFO
 - winuser/ICONINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ICONINFO
---

# ICONINFO structure

## -description

Contains information about an icon or a cursor.

## -struct-fields

### -field fIcon

Type: <b>BOOL</b>

Specifies whether this structure defines an icon or a cursor. A value of <b>TRUE</b> specifies an icon; <b>FALSE</b> specifies a cursor.

### -field xHotspot

Type: <b>DWORD</b>

The x-coordinate of a cursor's hot spot. If this structure defines an icon, the hot spot is always in the center of the icon, and this member is ignored.

### -field yHotspot

Type: <b>DWORD</b>

The y-coordinate of the cursor's hot spot. If this structure defines an icon, the hot spot is always in the center of the icon, and this member is ignored.

### -field hbmMask

Type: <b>HBITMAP</b>

A handle to the icon monochrome mask <a href="/windows/win32/gdi/bitmaps">bitmap</a>.

### -field hbmColor

Type: <b>HBITMAP</b>

A handle to the icon color <a href="/windows/win32/gdi/bitmaps">bitmap</a>.

## -remarks

For monochrome icons, the <b>hbmMask</b> is twice the height of the icon (with the AND mask on top and the XOR mask on the bottom), and <b>hbmColor</b> is <b>NULL</b>. Also, in this case the height should be an even multiple of two.

For color icons, the <b>hbmMask</b> and <b>hbmColor</b> bitmaps are the same size, each of which is the size of the icon.

You can use a <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> function to get contents of <b>hbmMask</b> and <b>hbmColor</b> in the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a> structure. The bitmap bits can be obtained with call to <a href="/windows/win32/api/wingdi/nf-wingdi-getdibits">GetDIBits</a> on the bitmaps in this structure.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>

<a href="/windows/desktop/menurc/icons">Icons</a>

<a href="/windows/desktop/gdi/bitmaps">Bitmaps</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>

<a href="/windows/win32/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>

<b>Reference</b>
