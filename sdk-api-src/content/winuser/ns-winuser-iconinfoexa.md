---
UID: NS:winuser._ICONINFOEXA
title: ICONINFOEXA (winuser.h)
description: Contains information about an icon or a cursor. Extends ICONINFO. Used by GetIconInfoEx.helpviewer_keywords: ["*PICONINFOEXA","ICONINFOEX","ICONINFOEX structure [Menus and Other Resources]","ICONINFOEXA","ICONINFOEXW","_win32_ICONINFOEX","_win32_iconinfoex_cpp","menurc.iconinfoex","winui._win32_iconinfoex","winuser/ICONINFOEX","winuser/ICONINFOEXA","winuser/ICONINFOEXW"]
old-location: menurc\iconinfoex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconstructures\iconinfoex.htm
ms.date: 12/05/2018
ms.keywords: '*PICONINFOEXA, ICONINFOEX, ICONINFOEX structure [Menus and Other Resources], ICONINFOEXA, ICONINFOEXW, _win32_ICONINFOEX, _win32_iconinfoex_cpp, menurc.iconinfoex, winui._win32_iconinfoex, winuser/ICONINFOEX, winuser/ICONINFOEXA, winuser/ICONINFOEXW'
f1_keywords:
- winuser/ICONINFOEX
dev_langs:
- c++
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
targetos: Windows
req.typenames: ICONINFOEXA, *PICONINFOEXA
req.redist: 
ms.custom: 19H1
---

# ICONINFOEXA structure


## -description


Contains information about an icon or a cursor. Extends <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a>. Used by <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-geticoninfoexa">GetIconInfoEx</a>.


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

The icon bitmask bitmap. If this structure defines a black and white icon, this bitmask is formatted so that the upper half is the icon AND bitmask and the lower half is the icon XOR bitmask. Under this condition, the height should be an even multiple of two. If this structure defines a color icon, this mask only defines the AND bitmask of the icon.


### -field hbmColor

Type: <b>HBITMAP</b>

A handle to the icon color bitmap. This member can be optional if this structure defines a black and white icon. The AND bitmask of <b>hbmMask</b> is applied with the <b>SRCAND</b> flag to the destination; subsequently, the color bitmap is applied (using XOR) to the destination by using the <b>SRCINVERT</b> flag.


### -field wResID

Type: <b>WORD</b>

The icon or cursor resource bits. These bits are typically loaded by calls to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> functions.


### -field szModName

Type: <b>TCHAR[MAX_PATH]</b>

The fully qualified path of the module.


### -field szResName

Type: <b>TCHAR[MAX_PATH]</b>

The fully qualified path of the resource.


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/icons">Icons</a>



<b>Reference</b>
 

 

