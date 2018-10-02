---
UID: NF:winuser.GetMenuItemInfoA
title: GetMenuItemInfoA function
author: windows-sdk-content
description: Retrieves information about a menu item.
old-location: menurc\getmenuiteminfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\getmenuiteminfo.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMenuItemInfo, GetMenuItemInfo function [Menus and Other Resources], GetMenuItemInfoA, GetMenuItemInfoW, _win32_GetMenuItemInfo, _win32_getmenuiteminfo_cpp, menurc.getmenuiteminfo, winui._win32_getmenuiteminfo, winuser/GetMenuItemInfo, winuser/GetMenuItemInfoA, winuser/GetMenuItemInfoW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetMenuItemInfoW (Unicode) and GetMenuItemInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
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
 - GetMenuItemInfo
 - GetMenuItemInfoA
 - GetMenuItemInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMenuItemInfoA function


## -description


Retrieves information about a menu item.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the menu item. 


### -param item [in]

Type: <b>UINT</b>

The identifier or position of the menu item to get information about. The meaning of this parameter depends on the value of <i>fByPosition</i>. 


### -param fByPosition [in]

Type: <b>BOOL</b>

The meaning of <i>uItem</i>. If this parameter is <b>FALSE</b>, <i>uItem</i> is a menu item identifier. Otherwise, it is a menu item position. See <a href="about_menus.htm">Accessing Menu Items Programmatically</a> for more information. 


### -param lpmii [in, out]

Type: <b>LPMENUITEMINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a> structure that specifies the information to retrieve and receives information about the menu item. Note that you must set the <b>cbSize</b> member to <code>sizeof(MENUITEMINFO)</code> before calling this function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



To retrieve a menu item of type <b>MFT_STRING</b>, first find the size of the string by setting the <b>dwTypeData</b> member of <a href="https://msdn.microsoft.com/43d30b39-c1e1-4711-97a2-b5bc29dad9df">MENUITEMINFO</a> to <b>NULL</b> and then calling <b>GetMenuItemInfo</b>. The value of <b>cch</b>+1 is the size needed. Then allocate a buffer of this size, place the pointer to the buffer in <b>dwTypeData</b>, increment <b>cch</b> by one, and then call <b>GetMenuItemInfo</b> once again to fill the buffer with the string.

If the retrieved menu item is of some other type, then <b>GetMenuItemInfo</b> sets the <b>dwTypeData</b> member to a value whose type is specified by the <b>fType</b><b>fType</b> member and sets <b>cch</b> to 0.


#### Examples

For an example, see <a href="using_menus.htm">Example of Owner-Drawn Menu Items</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e1c669c7-7b56-428a-8433-d926330e42e1">SetMenuItemInfo</a>
 

 

