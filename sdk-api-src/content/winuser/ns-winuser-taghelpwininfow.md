---
UID: NS:winuser.tagHELPWININFOW
title: tagHELPWININFOW
author: windows-sdk-content
description: Contains the size and position of either a primary or secondary Help window. An application can set this information by calling the WinHelp function with the HELP_SETWINPOS value.
old-location: shell\HELPWININFO_str.htm
tech.root: shell
ms.assetid: 0de0bf84-66f3-44bc-b4de-c2de7ca90cb2
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*LPHELPWININFOW, *PHELPWININFOW, HELPWININFO, HELPWININFO structure [Windows Shell], HELPWININFOW, LPHELPWININFO, LPHELPWININFO structure pointer [Windows Shell], PHELPWININFO, PHELPWININFO structure pointer [Windows Shell], SW_HIDE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, _win32_HELPWININFO_str, shell.HELPWININFO_str, tagHELPWININFOA, tagHELPWININFOW, winuser/HELPWININFO, winuser/LPHELPWININFO, winuser/PHELPWININFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - HELPWININFO
product: Windows
targetos: Windows
req.typenames: HELPWININFOW, *PHELPWININFOW, *LPHELPWININFOW
req.redist: 
---

# tagHELPWININFOW structure


## -description


Contains the size and position of either a primary or secondary Help window. An application can set this information by calling the <a href="https://msdn.microsoft.com/fce80bac-2a44-46e7-a87a-ef93f4599807">WinHelp</a> function with the HELP_SETWINPOS value.


## -struct-fields




### -field wStructSize

Type: <b>int</b>

The size of this structure, in bytes.


### -field x

Type: <b>int</b>

X-coordinate of the upper-left corner of the window, in screen coordinates.


### -field y

Type: <b>int</b>

Y-coordinate of the upper-left corner of the window, in screen coordinates.


### -field dx

Type: <b>int</b>

The width of the window, in pixels.


### -field dy

Type: <b>int</b>

The height of the window, in pixels.


### -field wMax

Type: <b>int</b>

Options for display of the window. Several values also determine the activation (focus) state of the window or other windows. This member must be one of the following values.



#### SW_HIDE

Hides the window and passes activation to another window.



#### SW_MINIMIZE

Minimizes the specified window and activates the top-level window in the z-order.



#### SW_RESTORE

Same as <b>SW_SHOWNORMAL</b>.



#### SW_SHOW

Activates a window and displays it in its current size and position.



#### SW_SHOWMAXIMIZED

Activates the window and displays it as a maximized window.



#### SW_SHOWMINIMIZED

Activates the window and displays it as an icon.



#### SW_SHOWMINNOACTIVE

Displays the window as an icon. The window that is currently active remains active.



#### SW_SHOWNA

Displays the window in its current state. The window that is currently active remains active.



#### SW_SHOWNOACTIVATE

Displays a window in its most recent size and position. The window that is currently active remains active.



#### SW_SHOWNORMAL

Activates and displays the window. Whether the window is minimized or maximized, Windows restores it to its original size and position.


### -field rgchMember

Type: <b>TCHAR[2]</b>

The name of the window.


##### - wMax.SW_HIDE

Hides the window and passes activation to another window.


##### - wMax.SW_MINIMIZE

Minimizes the specified window and activates the top-level window in the z-order.


##### - wMax.SW_RESTORE

Same as <b>SW_SHOWNORMAL</b>.


##### - wMax.SW_SHOW

Activates a window and displays it in its current size and position.


##### - wMax.SW_SHOWMAXIMIZED

Activates the window and displays it as a maximized window.


##### - wMax.SW_SHOWMINIMIZED

Activates the window and displays it as an icon.


##### - wMax.SW_SHOWMINNOACTIVE

Displays the window as an icon. The window that is currently active remains active.


##### - wMax.SW_SHOWNA

Displays the window in its current state. The window that is currently active remains active.


##### - wMax.SW_SHOWNOACTIVATE

Displays a window in its most recent size and position. The window that is currently active remains active.


##### - wMax.SW_SHOWNORMAL

Activates and displays the window. Whether the window is minimized or maximized, Windows restores it to its original size and position.


## -remarks



Windows Help divides the display into 1024 units in both the X and Y directions. To create a secondary window that fills the upper-left quadrant of the display, for example, an application would specify zero for the <b>x</b> and <b>y</b> members and 512 for the <b>dx</b> and <b>dy</b> members.

To calculate <b>wStructSize</b> properly, the actual size of the string to be stored at <b>rgchMember</b> must be known. Since <a href="70826d03-3451-41e4-bebb-a820ae66d53f">sizeof</a>(HELPWININFO) includes two <b>TCHARs</b> by definition, they must be taken into account in the final total. The following example shows the proper calculation of an instance of  <b>wStructSize</b>.

                


```
WORD wSize;
TCHAR *szWndName = TEXT("wnd_menu"); 
size_t NameLength;  
HRESULT hr;
HELPWININFO hwi;

// StringCbLength returns the length of the string without 
// the terminating null character.
hr = StringCbLength(szWndName, STRSAFE_MAX_CCH * sizeof(TCHAR), &NameLength);
    
if (SUCCEEDED(hr))
{
    // Add bytes to account for the name string's terminating null character.
    NameLength + sizeof(TCHAR);
    
    // Determine the size of HELPWININFO without the TCHAR array.
    wSize = sizeof(HELPWININFO) - (2 * sizeof(TCHAR));
    
    // Determine the total size of the final HELPWININFO structure.
    hwi.wStructSize = wSize + NameLength;
}
```




