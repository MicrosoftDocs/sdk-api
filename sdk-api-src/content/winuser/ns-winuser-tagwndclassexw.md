---
UID: NS:winuser.tagWNDCLASSEXW
title: tagWNDCLASSEXW
author: windows-sdk-content
description: Contains window class information.
old-location: winmsg\wndclassex.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windowclasses\windowclassreference\windowclassstructures\wndclassex.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPWNDCLASSEXW, *NPWNDCLASSEXW, *PWNDCLASSEXW, PWNDCLASSEX, PWNDCLASSEX structure pointer [Windows and Messages], WNDCLASSEX, WNDCLASSEX structure [Windows and Messages], WNDCLASSEXA, WNDCLASSEXW, _win32_WNDCLASSEX_str, _win32_wndclassex_str_cpp, tagWNDCLASSEXW, winmsg.wndclassex, winui._win32_wndclassex_str, winuser/PWNDCLASSEX, winuser/WNDCLASSEX, winuser/WNDCLASSEXA, winuser/WNDCLASSEXW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: WNDCLASSEXW, *PWNDCLASSEXW, *NPWNDCLASSEXW, *LPWNDCLASSEXW
req.redist: 
---

# tagWNDCLASSEXW structure


## -description


Contains window class information. It is used with the <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> and <a href="https://msdn.microsoft.com/en-us/library/ms633579(v=VS.85).aspx">GetClassInfoEx</a> 
			functions. 

The <b>WNDCLASSEX</b> structure is similar to the <a href="https://msdn.microsoft.com/en-us/library/ms633576(v=VS.85).aspx">WNDCLASS</a> structure. There are two differences. <b>WNDCLASSEX</b> includes the <b>cbSize</b> member, which specifies the size of the structure, and the <b>hIconSm</b> member, which contains a handle to a small icon associated with the window class.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size, in bytes, of this structure. Set this member to <code>sizeof(WNDCLASSEX)</code>. Be sure to set this member before calling the <a href="https://msdn.microsoft.com/en-us/library/ms633579(v=VS.85).aspx">GetClassInfoEx</a> function. 


### -field style

Type: <b>UINT</b>

The class style(s). This member can be any combination of the <a href="https://msdn.microsoft.com/en-us/library/ms633574(v=VS.85).aspx">Class Styles</a>. 


### -field lpfnWndProc

Type: <b>WNDPROC</b>

A pointer to the window procedure. You must use the <a href="https://msdn.microsoft.com/en-us/library/ms633571(v=VS.85).aspx">CallWindowProc</a> function to call the window procedure. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms633573(v=VS.85).aspx">WindowProc</a>. 


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
The system automatically deletes class background brushes when the class is unregistered by using <a href="https://msdn.microsoft.com/en-us/library/ms644899(v=VS.85).aspx">UnregisterClass</a>. An application should not delete these brushes. 

When this member is <b>NULL</b>, an application must paint its own background whenever it is requested to paint in its client area. To determine whether the background must be painted, an application can either process the 
						<a href="https://msdn.microsoft.com/en-us/library/ms648055(v=VS.85).aspx">WM_ERASEBKGND</a> message or test the 
						<b>fErase</b> member of the <a href="https://msdn.microsoft.com/1f8c6dd2-e511-48f2-8ab0-d2fadb1ce433">PAINTSTRUCT</a> structure filled by the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function. 


### -field lpszMenuName

Type: <b>LPCTSTR</b>

Pointer to a null-terminated character string that specifies the resource name of the class menu, as the name appears in the resource file. If you use an integer to identify the menu, use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro. If this member is <b>NULL</b>, windows belonging to this class have no default menu. 


### -field lpszClassName

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string or is an atom. If this parameter is an atom, it must be a class atom created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a> or <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> function. The atom must be in the low-order word of 
					<b>lpszClassName</b>; the high-order word must be zero. 
					

If <b>lpszClassName</b> is a string, it specifies the window class name. The class name can be any name registered with <a href="https://msdn.microsoft.com/en-us/library/ms633586(v=VS.85).aspx">RegisterClass</a> or <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>, or any of the predefined control-class names. 

The maximum length for <b>lpszClassName</b> is 256. If <b>lpszClassName</b> is greater than the maximum length, the <a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a> function will fail.


### -field hIconSm

Type: <b>HICON</b>

A handle to a small icon that is associated with the window class. If this member is <b>NULL</b>, the system searches the icon resource specified by the 
					<b>hIcon</b> member for an icon of the appropriate size to use as the small icon. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633579(v=VS.85).aspx">GetClassInfoEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms633587(v=VS.85).aspx">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644899(v=VS.85).aspx">UnregisterClass</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632596(v=VS.85).aspx">Window Classes</a>
 

 

