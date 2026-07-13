---
UID: NF:winuser.GetSysColorBrush
title: GetSysColorBrush function (winuser.h)
description: The GetSysColorBrush function retrieves a handle identifying a logical brush that corresponds to the specified color index.
helpviewer_keywords: ["GetSysColorBrush","GetSysColorBrush function [Windows GDI]","_win32_GetSysColorBrush","gdi.getsyscolorbrush","winuser/GetSysColorBrush"]
old-location: gdi\getsyscolorbrush.htm
tech.root: gdi
ms.assetid: 07a1d8e3-eae8-40ab-9d0f-4efa9fac0117
ms.date: 12/05/2018
ms.keywords: GetSysColorBrush, GetSysColorBrush function [Windows GDI], _win32_GetSysColorBrush, gdi.getsyscolorbrush, winuser/GetSysColorBrush
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
 - GetSysColorBrush
 - winuser/GetSysColorBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-gui-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-gui-l1-1-0.dll
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - user32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - GetSysColorBrush
req.apiset: ext-ms-win-ntuser-gui-l1-1-1 (introduced in Windows 8.1)
---

# GetSysColorBrush function


## -description

The <b>GetSysColorBrush</b> function retrieves a handle identifying a logical brush that corresponds to the specified color index.

## -parameters

### -param nIndex [in]

A color index. This value corresponds to the color used to paint one of the window elements. See <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> for system color index values.

## -returns

The return value identifies a logical brush if the <i>nIndex</i> parameter is supported by the current platform. Otherwise, it returns <b>NULL</b>.

## -remarks

A brush is a bitmap that the system uses to paint the interiors of filled shapes. An application can retrieve the current system colors by calling the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function. An application can set the current system colors by calling the <a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a> function.

An application must not register a window class for a window using a system brush. To register a window class with a system color, see the documentation of the <b>hbrBackground</b> member of the <a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a> or <a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a> structures.

System color brushes track changes in system colors. In other words, when the user changes a system color, the associated system color brush automatically changes to the new color.

To paint with a system color brush, an application should use <b>GetSysColorBrush</b> (nIndex) instead of <a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a> ( <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> (nIndex)), because <b>GetSysColorBrush</b> returns a cached brush instead of allocating a new one.

System color brushes are owned by the system so you don't need to destroy them. Although you don't need to delete the logical brush that <b>GetSysColorBrush</b> returns, no harm occurs by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>.

## -see-also

<a href="/windows/desktop/gdi/brush-functions">Brush Functions</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassa">WNDCLASS</a>



<a href="/windows/desktop/api/winuser/ns-winuser-wndclassexa">WNDCLASSEX</a>
