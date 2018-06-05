---
UID: NS:winuser.MENUITEMTEMPLATEHEADER
title: MENUITEMTEMPLATEHEADER
author: windows-sdk-content
description: Defines the header for a menu template. A complete menu template consists of a header and one or more menu item lists.
old-location: menurc\menuitemtemplateheader.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menustructures\menuitemtemplateheader.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PMENUITEMTEMPLATEHEADER, MENUITEMTEMPLATEHEADER, MENUITEMTEMPLATEHEADER structure [Menus and Other Resources], PMENUITEMTEMPLATEHEADER, PMENUITEMTEMPLATEHEADER structure pointer [Menus and Other Resources], _win32_MENUITEMTEMPLATEHEADER_str, _win32_menuitemtemplateheader_str_cpp, menurc.menuitemtemplateheader, winui._win32_menuitemtemplateheader_str, winuser/MENUITEMTEMPLATEHEADER, winuser/PMENUITEMTEMPLATEHEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MENUITEMTEMPLATEHEADER, *PMENUITEMTEMPLATEHEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winuser.h
api_name:
-	MENUITEMTEMPLATEHEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MENUITEMTEMPLATEHEADER structure


## -description


Defines the header for a menu template. A complete menu template consists of a header and one or more menu item lists. 


## -struct-fields




### -field versionNumber

Type: <b>WORD</b>

The version number. This member must be zero. 


### -field offset

Type: <b>WORD</b>

The offset, in bytes, from the end of the header. The menu item list begins at this offset. Usually, this member is zero, and the menu item list follows immediately after the header. 


## -remarks



One or more <a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a> structures are combined to form the menu item list. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/01736486-6dee-43fe-80a7-06c4cf13a23e">LoadMenuIndirect</a>



<a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

