---
UID: NF:winuser.SetMenuItemBitmaps
title: SetMenuItemBitmaps function (winuser.h)
description: Associates the specified bitmap with a menu item. Whether the menu item is selected or clear, the system displays the appropriate bitmap next to the menu item.
helpviewer_keywords: ["MF_BYCOMMAND","MF_BYPOSITION","SetMenuItemBitmaps","SetMenuItemBitmaps function [Menus and Other Resources]","_win32_SetMenuItemBitmaps","_win32_setmenuitembitmaps_cpp","menurc.setmenuitembitmaps","winui._win32_setmenuitembitmaps","winuser/SetMenuItemBitmaps"]
old-location: menurc\setmenuitembitmaps.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\menus\menureference\menufunctions\setmenuitembitmaps.htm
ms.date: 12/05/2018
ms.keywords: MF_BYCOMMAND, MF_BYPOSITION, SetMenuItemBitmaps, SetMenuItemBitmaps function [Menus and Other Resources], _win32_SetMenuItemBitmaps, _win32_setmenuitembitmaps_cpp, menurc.setmenuitembitmaps, winui._win32_setmenuitembitmaps, winuser/SetMenuItemBitmaps
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetMenuItemBitmaps
 - winuser/SetMenuItemBitmaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-menu-l1-1-3.dll
 - ext-ms-win-ntuser-menu-l1-1-2.dll
 - ext-ms-win-ntuser-menu-l1-1-1.dll
 - ext-ms-win-ntuser-menu-l1-1-0.dll
 - User32.dll
api_name:
 - SetMenuItemBitmaps
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

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If either the <i>hBitmapUnchecked</i> or 
				<i>hBitmapChecked</i> parameter is <b>NULL</b>, the system displays nothing next to the menu item for the corresponding check state. If both parameters are <b>NULL</b>, the system displays the default check-mark bitmap when the item is selected, and removes the bitmap when the item is not selected. 

When the menu is destroyed, these bitmaps are not destroyed; it is up to the application to destroy them. 

The selected and clear bitmaps should be monochrome. The system uses the Boolean AND operator to combine bitmaps with the menu so that the white part becomes transparent and the black part becomes the menu-item color. If you use color bitmaps, the results may be undesirable.

Use the <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> function with the <b>SM_CXMENUCHECK</b> and <b>SM_CYMENUCHECK</b> values to retrieve the bitmap dimensions.


#### Examples

For an example, see <a href="/windows/desktop/menurc/using-menus">Simulating Check Boxes in a Menu</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/menurc/menus">Menus</a>