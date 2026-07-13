---
UID: NS:winuser.tagHELPWININFOA
title: HELPWININFOA (winuser.h)
description: Contains the size and position of either a primary or secondary Help window. An application can set this information by calling the WinHelp function with the HELP_SETWINPOS value. (ANSI)
helpviewer_keywords: ["*LPHELPWININFOA","*PHELPWININFOA","HELPWININFO","HELPWININFO structure [Windows Shell]","HELPWININFOA","LPHELPWININFO","LPHELPWININFO structure pointer [Windows Shell]","PHELPWININFO","PHELPWININFO structure pointer [Windows Shell]","_win32_HELPWININFO_str","shell.HELPWININFO_str","tagHELPWININFOA","tagHELPWININFOW","winuser/HELPWININFO","winuser/LPHELPWININFO","winuser/PHELPWININFO"]
old-location: shell\HELPWININFO_str.htm
tech.root: shell
ms.assetid: 0de0bf84-66f3-44bc-b4de-c2de7ca90cb2
ms.date: 12/05/2018
ms.keywords: '*LPHELPWININFOA, *PHELPWININFOA, HELPWININFO, HELPWININFO structure [Windows Shell], HELPWININFOA, LPHELPWININFO, LPHELPWININFO structure pointer [Windows Shell], PHELPWININFO, PHELPWININFO structure pointer [Windows Shell], _win32_HELPWININFO_str, shell.HELPWININFO_str, tagHELPWININFOA, tagHELPWININFOW, winuser/HELPWININFO, winuser/LPHELPWININFO, winuser/PHELPWININFO'
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
targetos: Windows
req.typenames: HELPWININFOA, *PHELPWININFOA, *LPHELPWININFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHELPWININFOA
 - winuser/tagHELPWININFOA
 - PHELPWININFOA
 - winuser/PHELPWININFOA
 - HELPWININFOA
 - winuser/HELPWININFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - HELPWININFO
---

# HELPWININFOA structure


## -description

Contains the size and position of either a primary or secondary Help window. An application can set this information by calling the <a href="/windows/desktop/api/winuser/nf-winuser-winhelpa">WinHelp</a> function with the HELP_SETWINPOS value.

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

Options for display of the window. It can be any of the values that can be specified in the <i>nCmdShow</i> parameter for the <a href="/windows/desktop/api/winuser/nf-winuser-showwindow">ShowWindow</a> function.

### -field rgchMember

Type: <b>TCHAR[2]</b>

The name of the window.

## -remarks

Windows Help divides the display into 1024 units in both the X and Y directions. To create a secondary window that fills the upper-left quadrant of the display, for example, an application would specify zero for the <b>x</b> and <b>y</b> members and 512 for the <b>dx</b> and <b>dy</b> members.

To calculate <b>wStructSize</b> properly, the actual size of the string to be stored at <b>rgchMember</b> must be known. Since <a href="/previous-versions/0w557fh7(v=vs.85)">sizeof</a>(HELPWININFO) includes two <b>TCHARs</b> by definition, they must be taken into account in the final total. The following example shows the proper calculation of an instance of  <b>wStructSize</b>.

                


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





> [!NOTE]
> The winuser.h header defines HELPWININFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
