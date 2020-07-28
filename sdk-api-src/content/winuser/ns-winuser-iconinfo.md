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
f1_keywords:
- winuser/ICONINFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winuser.h
api_name:
- ICONINFO
targetos: Windows
req.typenames: ICONINFO
req.redist: 
ms.custom: 19H1
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

The icon bitmask bitmap. If this structure defines a black and white icon, this bitmask is formatted so that the upper half is the icon AND bitmask and the lower half is the icon XOR bitmask. Under this condition, the height should be an even multiple of two. If this structure defines a color icon, this mask only defines the AND bitmask of the icon. 


### -field hbmColor

Type: <b>HBITMAP</b>

A handle to the icon color bitmap. This member can be optional if this structure defines a black and white icon. The AND bitmask of <b>hbmMask</b> is applied with the <b>SRCAND</b> flag to the destination; subsequently, the color bitmap is applied (using XOR) to the destination by using the <b>SRCINVERT</b> flag.


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/icons">Icons</a>



<b>Reference</b>
 

 

