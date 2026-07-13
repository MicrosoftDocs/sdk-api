---
UID: NS:winuser.tagWNDCLASSA
title: WNDCLASSA (winuser.h)
description: Contains the window class attributes that are registered by the RegisterClass function. (ANSI)
helpviewer_keywords: ["*LPWNDCLASSA","*NPWNDCLASSA","*PWNDCLASSA","PWNDCLASS","PWNDCLASS structure pointer [Windows and Messages]","WNDCLASS","WNDCLASS structure [Windows and Messages]","WNDCLASSA","WNDCLASSW","_win32_WNDCLASS_str","_win32_wndclass_str_cpp","winmsg.wndclass","winui._win32_wndclass_str","winuser/PWNDCLASS","winuser/WNDCLASS","winuser/WNDCLASSA","winuser/WNDCLASSW"]
old-location: winmsg\wndclass.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassstructures\wndclass.htm
ms.date: 12/05/2018
ms.keywords: '*LPWNDCLASSA, *NPWNDCLASSA, *PWNDCLASSA, PWNDCLASS, PWNDCLASS structure pointer [Windows and Messages], WNDCLASS, WNDCLASS structure [Windows and Messages], WNDCLASSA, WNDCLASSW, _win32_WNDCLASS_str, _win32_wndclass_str_cpp, winmsg.wndclass, winui._win32_wndclass_str, winuser/PWNDCLASS, winuser/WNDCLASS, winuser/WNDCLASSA, winuser/WNDCLASSW'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNDCLASSW (Unicode) and WNDCLASSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WNDCLASSA, *PWNDCLASSA, *NPWNDCLASSA, *LPWNDCLASSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWNDCLASSA
 - winuser/tagWNDCLASSA
 - PWNDCLASSA
 - winuser/PWNDCLASSA
 - WNDCLASSA
 - winuser/WNDCLASSA
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
 - WNDCLASS
 - WNDCLASSA
 - WNDCLASSW
---

# WNDCLASSA structure


## -description

Contains the window class attributes that are registered by the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> function. 

This structure has been superseded by the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structure used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. You can still use <b>WNDCLASS</b> and <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> if you do not need to set the small icon associated with the window class.

## -struct-fields

### -field style

Type: <b>UINT</b>

The class style(s). This member can be any combination of the <a href="/windows/desktop/winmsg/about-window-classes#class-styles">Class Styles</a>.

### -field lpfnWndProc

Type: <b>WNDPROC</b>

A pointer to the window procedure. You must use the <a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a> function to call the window procedure. For more information, see <a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a>.

### -field cbClsExtra

Type: <b>int</b>

The number of extra bytes to allocate following the window-class structure. The system initializes the bytes to zero.

### -field cbWndExtra

Type: <b>int</b>

The number of extra bytes to allocate following the window instance. The system initializes the bytes to zero. If an application uses <b>WNDCLASS</b> to register a dialog box created by using the 
					<b>CLASS</b> directive in the resource file, it must set this member to <b>DLGWINDOWEXTRA</b>.

### -field hInstance

Type: <b>HINSTANCE</b>

A handle to the instance that contains the window procedure for the class.

### -field hIcon

Type: <b>HICON</b>

A handle to the class icon. This member must be a handle to an icon resource. If this member is <b>NULL</b>, the system provides a default icon.

### -field hCursor

Type: <b>HCURSOR</b>

A handle to the class cursor. This member must be a handle to a cursor resource. If this member is <b>NULL</b>, an application must explicitly set the cursor shape whenever the mouse moves into the application's window.

### -field hbrBackground

Type: <b>HBRUSH</b>

A handle to the class background brush. This member can be a handle to the physical brush to be used for painting the background, or it can be a color value. A color value must be one of the following standard system colors (the value 1 must be added to the chosen color). If a color value is given, you must convert it to one of the following 
<b>HBRUSH</b> types: 


<ul>
<li>COLOR_ACTIVEBORDER</li>
<li>COLOR_ACTIVECAPTION</li>
<li>COLOR_APPWORKSPACE</li>
<li>COLOR_BACKGROUND</li>
<li>COLOR_BTNFACE</li>
<li>COLOR_BTNSHADOW</li>
<li>COLOR_BTNTEXT</li>
<li>COLOR_CAPTIONTEXT</li>
<li>COLOR_GRAYTEXT</li>
<li>COLOR_HIGHLIGHT</li>
<li>COLOR_HIGHLIGHTTEXT</li>
<li>COLOR_INACTIVEBORDER</li>
<li>COLOR_INACTIVECAPTION</li>
<li>COLOR_MENU</li>
<li>COLOR_MENUTEXT</li>
<li>COLOR_SCROLLBAR</li>
<li>COLOR_WINDOW</li>
<li>COLOR_WINDOWFRAME</li>
<li>COLOR_WINDOWTEXT </li>
</ul>
The system automatically deletes class background brushes when the class is unregistered by using <a href="/windows/desktop/api/winuser/nf-winuser-unregisterclassa">UnregisterClass</a>. An application should not delete these brushes. 

When this member is <b>NULL</b>, an application must paint its own background whenever it is requested to paint in its client area. To determine whether the background must be painted, an application can either process the 
						<a href="/windows/desktop/winmsg/wm-erasebkgnd">WM_ERASEBKGND</a> message or test the 
						<b>fErase</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-paintstruct">PAINTSTRUCT</a> structure filled by the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function.

### -field lpszMenuName

Type: <b>LPCTSTR</b>

The resource name of the class menu, as the name appears in the resource file. If you use an integer to identify the menu, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. If this member is <b>NULL</b>, windows belonging to this class have no default menu.

### -field lpszClassName

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string or is an atom. If this parameter is an atom, it must be a class atom created by a previous call to the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. The atom must be in the low-order word of 
					<b>lpszClassName</b>; the high-order word must be zero. 
					

If <b>lpszClassName</b> is a string, it specifies the window class name. The class name can be any name registered with <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>, or any of the predefined control-class names. 

The maximum length for <b>lpszClassName</b> is 256. If <b>lpszClassName</b> is greater than the maximum length, the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> function will fail.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/winuser/ns-winuser-paintstruct">PAINTSTRUCT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregisterclassa">UnregisterClass</a>



<a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>



<a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a>

## -remarks

> [!NOTE]
> The winuser.h header defines WNDCLASS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
