---
UID: NS:winuser.tagWNDCLASSEXW
title: WNDCLASSEXW (winuser.h)
description: Contains window class information. (Unicode)
helpviewer_keywords: ["*LPWNDCLASSEXW","*NPWNDCLASSEXW","*PWNDCLASSEXW","PWNDCLASSEX","PWNDCLASSEX structure pointer [Windows and Messages]","WNDCLASSEX","WNDCLASSEX structure [Windows and Messages]","WNDCLASSEXA","WNDCLASSEXW","_win32_WNDCLASSEX_str","_win32_wndclassex_str_cpp","winmsg.wndclassex","winui._win32_wndclassex_str","winuser/PWNDCLASSEX","winuser/WNDCLASSEX","winuser/WNDCLASSEXA","winuser/WNDCLASSEXW"]
old-location: winmsg\wndclassex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassstructures\wndclassex.htm
ms.date: 12/05/2018
ms.keywords: '*LPWNDCLASSEXW, *NPWNDCLASSEXW, *PWNDCLASSEXW, PWNDCLASSEX, PWNDCLASSEX structure pointer [Windows and Messages], WNDCLASSEX, WNDCLASSEX structure [Windows and Messages], WNDCLASSEXA, WNDCLASSEXW, _win32_WNDCLASSEX_str, _win32_wndclassex_str_cpp, winmsg.wndclassex, winui._win32_wndclassex_str, winuser/PWNDCLASSEX, winuser/WNDCLASSEX, winuser/WNDCLASSEXA, winuser/WNDCLASSEXW'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNDCLASSEXW (Unicode) and WNDCLASSEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WNDCLASSEXW, *PWNDCLASSEXW, *NPWNDCLASSEXW, *LPWNDCLASSEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWNDCLASSEXW
 - winuser/tagWNDCLASSEXW
 - PWNDCLASSEXW
 - winuser/PWNDCLASSEXW
 - WNDCLASSEXW
 - winuser/WNDCLASSEXW
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
 - WNDCLASSEX
 - WNDCLASSEXA
 - WNDCLASSEXW
---

# WNDCLASSEXW structure


## -description

Contains window class information. It is used with the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> and <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa">GetClassInfoEx</a> 
			functions. 

The <b>WNDCLASSEX</b> structure is similar to the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a> structure. There are two differences. <b>WNDCLASSEX</b> includes the <b>cbSize</b> member, which specifies the size of the structure, and the <b>hIconSm</b> member, which contains a handle to a small icon associated with the window class.

## -struct-fields

### -field cbSize

Type: <b>UINT</b>

The size, in bytes, of this structure. Set this member to <code>sizeof(WNDCLASSEX)</code>. Be sure to set this member before calling the <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa">GetClassInfoEx</a> function.

### -field style

Type: <b>UINT</b>

The class style(s). This member can be any combination of the <a href="/windows/win32/winmsg/window-class-styles">Class Styles</a>.

### -field lpfnWndProc

Type: <b>WNDPROC</b>

A pointer to the window procedure. You must use the <a href="/windows/desktop/api/winuser/nf-winuser-callwindowproca">CallWindowProc</a> function to call the window procedure. For more information, see <a href="/windows/win32/api/winuser/nc-winuser-wndproc">WindowProc</a>.

### -field cbClsExtra

Type: <b>int</b>

The number of extra bytes to allocate following the window-class structure. The system initializes the bytes to zero.

### -field cbWndExtra

Type: <b>int</b>

The number of extra bytes to allocate following the window instance. The system initializes the bytes to zero. If an application uses <b>WNDCLASSEX</b> to register a dialog box created by using the 
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

A handle to the class background brush. This member can be a handle to the brush to be used for painting the background, or it can be a color value. A color value must be one of the following standard system colors (the value 1 must be added to the chosen color). If a color value is given, you must convert it to one of the following 
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

Pointer to a null-terminated character string that specifies the resource name of the class menu, as the name appears in the resource file. If you use an integer to identify the menu, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro. If this member is <b>NULL</b>, windows belonging to this class have no default menu.

### -field lpszClassName

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string or is an atom. If this parameter is an atom, it must be a class atom created by a previous call to the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function. The atom must be in the low-order word of 
					<b>lpszClassName</b>; the high-order word must be zero. 
					

If <b>lpszClassName</b> is a string, it specifies the window class name. The class name can be any name registered with <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> or <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>, or any of the predefined control-class names. 

The maximum length for <b>lpszClassName</b> is 256. If <b>lpszClassName</b> is greater than the maximum length, the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function will fail.

### -field hIconSm

Type: <b>HICON</b>

A handle to a small icon that is associated with the window class. If this member is <b>NULL</b>, the system searches the icon resource specified by the 
					<b>hIcon</b> member for an icon of the appropriate size to use as the small icon.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa">GetClassInfoEx</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-unregisterclassa">UnregisterClass</a>



<a href="/windows/desktop/winmsg/window-classes">Window Classes</a>

## -remarks

> [!NOTE]
> The winuser.h header defines WNDCLASSEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
