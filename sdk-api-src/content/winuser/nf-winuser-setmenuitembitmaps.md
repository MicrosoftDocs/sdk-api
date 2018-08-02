---
UID: NF:winuser.SetMenuItemBitmaps
title: SetMenuItemBitmaps function
author: windows-sdk-content
description: Associates the specified bitmap with a menu item. Whether the menu item is selected or clear, the system displays the appropriate bitmap next to the menu item.
old-location: menurc\setmenuitembitmaps.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\setmenuitembitmaps.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: MF_BYCOMMAND, MF_BYPOSITION, SetMenuItemBitmaps, SetMenuItemBitmaps function [Menus and Other Resources], _win32_SetMenuItemBitmaps, _win32_setmenuitembitmaps_cpp, menurc.setmenuitembitmaps, winui._win32_setmenuitembitmaps, winuser/SetMenuItemBitmaps
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetMenuItemBitmaps
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetMenuItemBitmaps function


## -description


Associates the specified bitmap with a menu item. Whether the menu item is selected or clear, the system displays the appropriate bitmap next to the menu item. 


## -parameters




### -param hMenu [in]

Type: <b>HMENU</b>

A handle to the menu containing the item to receive new check-mark bitmaps. 


### -param uPosition [in]

Type: <b>UINT</b>

The menu item to be changed, as determined by the <i>uFlags</i> parameter. 


### -param uFlags [in]

Type: <b>UINT</b>

Specifies how the <i>uPosition</i> parameter is to be interpreted. The <i>uFlags</i> parameter must be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_BYCOMMAND"></a><a id="mf_bycommand"></a><dl>
<dt><b>MF_BYCOMMAND</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uPosition</i> gives the identifier of the menu item. If neither <b>MF_BYCOMMAND</b> nor <b>MF_BYPOSITION</b> is specified, <b>MF_BYCOMMAND</b> is the default flag.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_BYPOSITION"></a><a id="mf_byposition"></a><dl>
<dt><b>MF_BYPOSITION</b></dt>
<dt>0x00000400L</dt>
</dl>
</td>
<td width="60%">
Indicates that <i>uPosition</i> gives the zero-based relative position of the menu item.

</td>
</tr>
</table>
 


### -param hBitmapUnchecked [in, optional]

Type: <b>HBITMAP</b>

A handle to the bitmap displayed when the menu item is not selected. 


### -param hBitmapChecked [in, optional]

Type: <b>HBITMAP</b>

A handle to the bitmap displayed when the menu item is selected. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



If either the <i>hBitmapUnchecked</i> or 
				<i>hBitmapChecked</i> parameter is <b>NULL</b>, the system displays nothing next to the menu item for the corresponding check state. If both parameters are <b>NULL</b>, the system displays the default check-mark bitmap when the item is selected, and removes the bitmap when the item is not selected. 

When the menu is destroyed, these bitmaps are not destroyed; it is up to the application to destroy them. 

The selected and clear bitmaps should be monochrome. The system uses the Boolean AND operator to combine bitmaps with the menu so that the white part becomes transparent and the black part becomes the menu-item color. If you use color bitmaps, the results may be undesirable.

Use the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function with the <b>CXMENUCHECK</b> and <b>CYMENUCHECK</b> values to retrieve the bitmap dimensions.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms647558(v=VS.85).aspx">Simulating Check Boxes in a Menu</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646977(v=VS.85).aspx">Menus</a>
 

 

