---
UID: NS:winuser.tagHELPWININFOA
title: HELPWININFOA (winuser.h)
description: Contains the size and position of either a primary or secondary Help window. An application can set this information by calling the WinHelp function with the HELP_SETWINPOS value.helpviewer_keywords: ["*LPHELPWININFOA","*PHELPWININFOA","HELPWININFO","HELPWININFO structure [Windows Shell]","HELPWININFOA","LPHELPWININFO","LPHELPWININFO structure pointer [Windows Shell]","PHELPWININFO","PHELPWININFO structure pointer [Windows Shell]","SW_HIDE","SW_MINIMIZE","SW_RESTORE","SW_SHOW","SW_SHOWMAXIMIZED","SW_SHOWMINIMIZED","SW_SHOWMINNOACTIVE","SW_SHOWNA","SW_SHOWNOACTIVATE","SW_SHOWNORMAL","_win32_HELPWININFO_str","shell.HELPWININFO_str","tagHELPWININFOA","tagHELPWININFOW","winuser/HELPWININFO","winuser/LPHELPWININFO","winuser/PHELPWININFO"]
old-location: shell\HELPWININFO_str.htm
tech.root: shell
ms.assetid: 0de0bf84-66f3-44bc-b4de-c2de7ca90cb2
ms.date: 12/05/2018
ms.keywords: '*LPHELPWININFOA, *PHELPWININFOA, HELPWININFO, HELPWININFO structure [Windows Shell], HELPWININFOA, LPHELPWININFO, LPHELPWININFO structure pointer [Windows Shell], PHELPWININFO, PHELPWININFO structure pointer [Windows Shell], SW_HIDE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, _win32_HELPWININFO_str, shell.HELPWININFO_str, tagHELPWININFOA, tagHELPWININFOW, winuser/HELPWININFO, winuser/LPHELPWININFO, winuser/PHELPWININFO'
f1_keywords:
- winuser/HELPWININFO
dev_langs:
- c++
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
targetos: Windows
req.typenames: HELPWININFOA, *PHELPWININFOA, *LPHELPWININFOA
req.redist: 
ms.custom: 19H1
---

# HELPWININFOA structure


## -description


Contains the size and position of either a primary or secondary Help window. An application can set this information by calling the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-winhelpa">WinHelp</a> function with the HELP_SETWINPOS value.


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


## -remarks



Windows Help divides the display into 1024 units in both the X and Y directions. To create a secondary window that fills the upper-left quadrant of the display, for example, an application would specify zero for the <b>x</b> and <b>y</b> members and 512 for the <b>dx</b> and <b>dy</b> members.

To calculate <b>wStructSize</b> properly, the actual size of the string to be stored at <b>rgchMember</b> must be known. Since <a href="https://docs.microsoft.com/previous-versions/0w557fh7(v=vs.85)">sizeof</a>(HELPWININFO) includes two <b>TCHARs</b> by definition, they must be taken into account in the final total. The following example shows the proper calculation of an instance of  <b>wStructSize</b>.

                


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




