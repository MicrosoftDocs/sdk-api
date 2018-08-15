---
UID: NS:winuser._ICONINFO
title: "_ICONINFO"
author: windows-sdk-content
description: Contains information about an icon or a cursor.
old-location: menurc\iconinfo.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconstructures\iconinfo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PICONINFO, ICONINFO, ICONINFO structure [Menus and Other Resources], PICONINFO, PICONINFO structure pointer [Menus and Other Resources], _ICONINFO, _win32_ICONINFO_str, _win32_iconinfo_str_cpp, menurc.iconinfo, winui._win32_iconinfo_str, winuser/ICONINFO, winuser/PICONINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: ICONINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ICONINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _ICONINFO structure


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



<a href="https://msdn.microsoft.com/en-us/library/ms648062(v=VS.85).aspx">CreateIconIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648070(v=VS.85).aspx">GetIconInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646973(v=VS.85).aspx">Icons</a>



<b>Reference</b>
 

 

