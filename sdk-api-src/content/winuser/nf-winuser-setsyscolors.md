---
UID: NF:winuser.SetSysColors
title: SetSysColors function (winuser.h)
description: Sets the colors for the specified display elements.
helpviewer_keywords: ["SetSysColors","SetSysColors function [Windows and Messages]","_win32_setsyscolors","base.changing_the_colors_of_window_elements","base.setsyscolors","winmsg.setsyscolors","winui.setsyscolors","winuser/SetSysColors"]
old-location: winmsg\setsyscolors.htm
tech.root: winmsg
ms.assetid: 41a7a96c-f9d1-44e3-a7e1-fd7d155c4ed0
ms.date: 12/05/2018
ms.keywords: SetSysColors, SetSysColors function [Windows and Messages], _win32_setsyscolors, base.changing_the_colors_of_window_elements, base.setsyscolors, winmsg.setsyscolors, winui.setsyscolors, winuser/SetSysColors
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
 - SetSysColors
 - winuser/SetSysColors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-syscolors-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-rtcore-ntuser-sysparams-l1-1-0.dll
 - Ext-MS-Win-NTUser-SysParaMS-Ext-L1-1-0.dll
api_name:
 - SetSysColors
---

# SetSysColors function


## -description

Sets the colors for the specified display elements. Display elements are the various parts of a window and the display that appear on the system display screen.

## -parameters

### -param cElements [in]

Type: <b>int</b>

The number of display elements in the <i>lpaElements</i> array.

### -param lpaElements [in]

Type: <b>const INT*</b>

An array of integers that specify the display elements to be changed. For a list of display elements, see 
<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>.

### -param lpaRgbValues [in]

Type: <b>const COLORREF*</b>

An array of 
<a href="/windows/desktop/gdi/colorref">COLORREF</a> values that contain the new red, green, blue (RGB) color values for the display elements in the array pointed to by the <i>lpaElements</i> parameter.

To generate a 
<a href="/windows/desktop/gdi/colorref">COLORREF</a>, use the 
<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SetSysColors</b> function sends a 
<a href="/windows/desktop/gdi/wm-syscolorchange">WM_SYSCOLORCHANGE</a> message to all windows to inform them of the change in color. It also directs the system to repaint the affected portions of all currently visible windows.

It is best to respect the color settings specified by the user. If you are writing an application to enable the user to change the colors, then it is appropriate to use this function. However, this 
function affects only the current session. The new colors are not saved when the system terminates.


#### Examples

The following example demonstrates the use of  the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> and <b>SetSysColors</b> functions.  First, the example uses <b>GetSysColor</b> to retrieve the colors of the window background and active caption and displays the red, green, blue (RGB) values in hexadecimal notation. Next, example uses <b>SetSysColors</b> to change the color of the window background to light gray and the active title bars to dark purple. After a 10-second delay, the example restores the previous colors for these elements using <a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a>.


```
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "user32.lib")

void main()
{
    int aElements[2] = {COLOR_WINDOW, COLOR_ACTIVECAPTION};
    DWORD aOldColors[2];
    DWORD aNewColors[2];

    // Get the current color of the window background. 
 
    aOldColors[0] = GetSysColor(aElements[0]); 

    printf("Current window color: {0x%x, 0x%x, 0x%x}\n", 
        GetRValue(aOldColors[0]), 
        GetGValue(aOldColors[0]), 
        GetBValue(aOldColors[0]));

    // Get the current color of the active caption. 
 
    aOldColors[1] = GetSysColor(aElements[1]); 

    printf("Current active caption color: {0x%x, 0x%x, 0x%x}\n", 
        GetRValue(aOldColors[1]), 
        GetGValue(aOldColors[1]), 
        GetBValue(aOldColors[1]));

    // Define new colors for the elements

    aNewColors[0] = RGB(0x80, 0x80, 0x80);  // light gray 
    aNewColors[1] = RGB(0x80, 0x00, 0x80);  // dark purple 

    printf("\nNew window color: {0x%x, 0x%x, 0x%x}\n", 
        GetRValue(aNewColors[0]), 
        GetGValue(aNewColors[0]), 
        GetBValue(aNewColors[0]));

    printf("New active caption color: {0x%x, 0x%x, 0x%x}\n", 
        GetRValue(aNewColors[1]), 
        GetGValue(aNewColors[1]), 
        GetBValue(aNewColors[1]));

    // Set the elements defined in aElements to the colors defined
    // in aNewColors

    SetSysColors(2, aElements, aNewColors); 

    printf("\nWindow background and active border have been changed.\n");
    printf("Reverting to previous colors in 10 seconds...\n");

    Sleep(10000);    

    // Restore the elements to their original colors

    SetSysColors(2, aElements, aOldColors); 
}
```

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>