---
UID: NS:winuser.tagALTTABINFO
title: ALTTABINFO (winuser.h)
description: Contains status information for the application-switching (ALT+TAB) window.
helpviewer_keywords: ["*LPALTTABINFO","*PALTTABINFO","ALTTABINFO","ALTTABINFO structure [Windows and Messages]","LPALTTABINFO","LPALTTABINFO structure pointer [Windows and Messages]","PALTTABINFO","PALTTABINFO structure pointer [Windows and Messages]","_win32_ALTTABINFO_str","_win32_alttabinfo_str_cpp","winmsg.alttabinfo","winui._win32_alttabinfo_str","winuser/ALTTABINFO","winuser/LPALTTABINFO","winuser/PALTTABINFO"]
old-location: winmsg\alttabinfo.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\alttabinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPALTTABINFO, *PALTTABINFO, ALTTABINFO, ALTTABINFO structure [Windows and Messages], LPALTTABINFO, LPALTTABINFO structure pointer [Windows and Messages], PALTTABINFO, PALTTABINFO structure pointer [Windows and Messages], _win32_ALTTABINFO_str, _win32_alttabinfo_str_cpp, winmsg.alttabinfo, winui._win32_alttabinfo_str, winuser/ALTTABINFO, winuser/LPALTTABINFO, winuser/PALTTABINFO'
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
req.typenames: ALTTABINFO, *PALTTABINFO, *LPALTTABINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagALTTABINFO
 - winuser/tagALTTABINFO
 - PALTTABINFO
 - winuser/PALTTABINFO
 - ALTTABINFO
 - winuser/ALTTABINFO
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
 - ALTTABINFO
---

# ALTTABINFO structure


## -description

Contains status information for the application-switching (ALT+TAB) window.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of the structure. The caller must set this to <code>sizeof(ALTTABINFO)</code>.

### -field cItems

Type: <b>int</b>

The number of items in the window.

### -field cColumns

Type: <b>int</b>

The number of columns in the window.

### -field cRows

Type: <b>int</b>

The number of rows in the window.

### -field iColFocus

Type: <b>int</b>

The column of the item that has the focus.

### -field iRowFocus

Type: <b>int</b>

The row of the item that has the focus.

### -field cxItem

Type: <b>int</b>

The width of each icon in the application-switching window.

### -field cyItem

Type: <b>int</b>

The height of each icon in the application-switching window.

### -field ptStart

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The top-left corner of the first icon.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getalttabinfoa">GetAltTabInfo</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>