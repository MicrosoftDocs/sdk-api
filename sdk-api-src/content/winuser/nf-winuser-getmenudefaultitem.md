---
UID: NF:winuser.GetMenuDefaultItem
title: GetMenuDefaultItem function
author: windows-sdk-content
description: Determines the default menu item on the specified menu.
old-location: menurc\getmenudefaultitem.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenudefaultitem.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GMDI_GOINTOPOPUPS, GMDI_USEDISABLED, GetMenuDefaultItem, GetMenuDefaultItem function [Menus and Other Resources], _win32_GetMenuDefaultItem, _win32_getmenudefaultitem_cpp, menurc.getmenudefaultitem, winui._win32_getmenudefaultitem, winuser/GetMenuDefaultItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-0.dll
 - Ext-MS-Win-NTUser-Menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - Ext-MS-Win-NTUser-Menu-L1-1-3.dll
api_name:
 - GetMenuDefaultItem
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetMenuDefaultItem function


## -description


Determines the default menu item on the specified menu.


## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu for which to retrieve the default menu item. 


### -param fByPos [in]

Type: <b>UINT</b>

Indicates whether to retrieve the menu item's identifier or its position. If this parameter is <b>FALSE</b>, the identifier is returned. Otherwise, the position is returned. 


### -param gmdiFlags [in]

Type: <b>UINT</b>

Indicates how the function should search for menu items. This parameter can be zero or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GMDI_GOINTOPOPUPS"></a><a id="gmdi_gointopopups"></a><dl>
<dt><b>GMDI_GOINTOPOPUPS</b></dt>
<dt>0x0002L</dt>
</dl>
</td>
<td width="60%">
If the default item is one that opens a submenu, the function is to search recursively in the corresponding submenu. If the submenu has no default item, the return value identifies the item that opens the submenu. By default, the function returns the first default item on the specified menu, regardless of whether it is an item that opens a submenu.

</td>
</tr>
<tr>
<td width="40%"><a id="GMDI_USEDISABLED"></a><a id="gmdi_usedisabled"></a><dl>
<dt><b>GMDI_USEDISABLED</b></dt>
<dt>0x0001L</dt>
</dl>
</td>
<td width="60%">
The function is to return a default item, even if it is disabled. By default, the function skips disabled or grayed items.

</td>
</tr>
</table>
 


## -returns



Type: <b>UINT</b>

If the function succeeds, the return value is the identifier or position of the menu item.

If the function fails, the return value is -1. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e679f714-6298-4425-8a64-2029ae7b1326">SetMenuDefaultItem</a>
 

 

