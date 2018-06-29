---
UID: NF:winuser.CheckMenuRadioItem
title: CheckMenuRadioItem function
author: windows-sdk-content
description: Checks a specified menu item and makes it a radio item. At the same time, the function clears all other menu items in the associated group and clears the radio-item type flag for those items.
old-location: menurc\checkmenuradioitem.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\checkmenuradioitem.htm
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CheckMenuRadioItem, CheckMenuRadioItem function [Menus and Other Resources], _win32_CheckMenuRadioItem, _win32_checkmenuradioitem_cpp, menurc.checkmenuradioitem, winui._win32_checkmenuradioitem, winuser/CheckMenuRadioItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: POINTER_DEVICE_TYPE
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
 - CheckMenuRadioItem
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CheckMenuRadioItem function


## -description


Checks a specified menu item and makes it a radio item. At the same time, the function clears all other menu items in the associated group and clears the radio-item type flag for those items.


## -parameters




### -param hmenu [in]

Type: <b>HMENU</b>

A handle to the menu that contains the group of menu items. 


### -param first

TBD


### -param last

TBD


### -param check

TBD


### -param flags

TBD




#### - idCheck [in]

Type: <b>UINT</b>

The identifier or position of the menu item to check. 


#### - idFirst [in]

Type: <b>UINT</b>

The identifier or position of the first menu item in the group. 


#### - idLast [in]

Type: <b>UINT</b>

The identifier or position of the last menu item in the group. 


#### - uFlags [in]

Type: <b>UINT</b>

Indicates the meaning of <i>idFirst</i>, <i>idLast</i>, and <i>idCheck</i>. If this parameter is <b>MF_BYCOMMAND</b>, the other parameters specify menu item identifiers. If it is <b>MF_BYPOSITION</b>, the other parameters specify the menu item positions. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



The <b>CheckMenuRadioItem</b> function sets the <b>MFT_RADIOCHECK</b> type flag and the <b>MFS_CHECKED</b> state for the item specified by <i>idCheck</i> and, at the same time, clears both flags for all other items in the group. The selected item is displayed using a bullet bitmap instead of a check-mark bitmap.

For more information about menu item type and state flags, see the <a href="https://msdn.microsoft.com/library/ms647578(v=VS.85).aspx">MENUITEMINFO</a> structure.


#### Examples

For an example, see Example of <a href="https://msdn.microsoft.com/library/ms647558(v=VS.85).aspx">Example of Using Custom Checkmark Bitmaps</a>. 

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms647578(v=VS.85).aspx">MENUITEMINFO</a>



<a href="https://msdn.microsoft.com/library/ms646977(v=VS.85).aspx">Menus</a>



<b>Reference</b>
 

 

