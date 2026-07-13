---
UID: NS:winuser._ICONINFOEXA
title: ICONINFOEXA (winuser.h)
description: Contains information about an icon or a cursor. Extends ICONINFO. Used by GetIconInfoEx. (ANSI)
helpviewer_keywords: ["*PICONINFOEXA","ICONINFOEX","ICONINFOEX structure [Menus and Other Resources]","ICONINFOEXA","ICONINFOEXW","_win32_ICONINFOEX","_win32_iconinfoex_cpp","menurc.iconinfoex","winui._win32_iconinfoex","winuser/ICONINFOEX","winuser/ICONINFOEXA","winuser/ICONINFOEXW"]
old-location: menurc\iconinfoex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconstructures\iconinfoex.htm
ms.date: 12/05/2018
ms.keywords: '*PICONINFOEXA, ICONINFOEX, ICONINFOEX structure [Menus and Other Resources], ICONINFOEXA, ICONINFOEXW, _win32_ICONINFOEX, _win32_iconinfoex_cpp, menurc.iconinfoex, winui._win32_iconinfoex, winuser/ICONINFOEX, winuser/ICONINFOEXA, winuser/ICONINFOEXW'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ICONINFOEXW (Unicode) and ICONINFOEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ICONINFOEXA, *PICONINFOEXA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ICONINFOEXA
 - winuser/_ICONINFOEXA
 - PICONINFOEXA
 - winuser/PICONINFOEXA
 - ICONINFOEXA
 - winuser/ICONINFOEXA
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
 - ICONINFOEX
 - ICONINFOEXA
 - ICONINFOEXW
---

# ICONINFOEXA structure

## -description

Contains information about an icon or a cursor. Extends <a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a>. Used by <a href="/windows/desktop/api/winuser/nf-winuser-geticoninfoexa">GetIconInfoEx</a>.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size, in bytes, of this structure.

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

### -field wResID

Type: <b>WORD</b>

Resource identifier of the resource in <b>szModName</b> module. If the icon or cursor was loaded by name, then <b>wResID</b> is zero and <b>szResName</b> contains the resource name.

You can use <a href="/windows/win32/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>(wResID) macro to convert resource identifier to a resource name type compatible with the <a href="/windows/win32/menurc/resources-functions">resource-management functions</a>.

### -field szModName

Type: <b>TCHAR[MAX_PATH]</b>

Name of the module from which an icon or a cursor was loaded.

You can use <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a> function to convert it to the module handle compatible with the <a href="/windows/win32/menurc/resources-functions">resource-management functions</a>.

### -field szResName

Type: <b>TCHAR[MAX_PATH]</b>

Resource name of the resource in <b>szModName</b> module. 

## -remarks

For monochrome icons, the <b>hbmMask</b> is twice the height of the icon (with the AND mask on top and the XOR mask on the bottom), and <b>hbmColor</b> is <b>NULL</b>. Also, in this case the height should be an even multiple of two.

For color icons, the <b>hbmMask</b> and <b>hbmColor</b> bitmaps are the same size, each of which is the size of the icon.

You can use a <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> function to get contents of <b>hbmMask</b> and <b>hbmColor</b> in the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a> structure. The bitmap bits can be obtained with call to <a href="/windows/win32/api/wingdi/nf-wingdi-getdibits">GetDIBits</a> on the bitmaps in this structure.

<b>ICONINFOEX</b> is an extended version of <b>ICONINFO</b> structure with additional <b>szModName</b>/<b>szResName</b>/<b>wResID</b> members that can be used to query an icon or cursor resource bits. These bits are typically loaded by calls to the <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-findresourcew">FindResource</a>, <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>, <a href="/windows/win32/api/libloaderapi/nf-libloaderapi-lockresource">LockResource</a> and <a href="/windows/win32/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a> functions.

> [!NOTE]
> The winuser.h header defines ICONINFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>

<a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>

<a href="/windows/desktop/menurc/icons">Icons</a>

<a href="/windows/desktop/gdi/bitmaps">Bitmaps</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>

<a href="/windows/win32/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>

<b>Reference</b>
