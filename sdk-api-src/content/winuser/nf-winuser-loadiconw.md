---
UID: NF:winuser.LoadIconW
title: LoadIconW function (winuser.h)
description: Loads the specified icon resource from the executable (.exe) file associated with an application instance. (Unicode)
helpviewer_keywords: ["LoadIcon", "LoadIcon function [Menus and Other Resources]", "LoadIconW", "_win32_LoadIcon", "_win32_loadicon_cpp", "menurc.loadicon", "winui._win32_loadicon", "winuser/LoadIcon", "winuser/LoadIconW"]
old-location: menurc\loadicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\loadicon.htm
ms.date: 12/05/2018
ms.keywords: LoadIcon, LoadIcon function [Menus and Other Resources], LoadIconA, LoadIconW, _win32_LoadIcon, _win32_loadicon_cpp, menurc.loadicon, winui._win32_loadicon, winuser/LoadIcon, winuser/LoadIconA, winuser/LoadIconW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadIconW (Unicode) and LoadIconA (ANSI)
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
 - LoadIconW
 - winuser/LoadIconW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - User32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - LoadIcon
 - LoadIconA
 - LoadIconW
req.apiset: ext-ms-win-ntuser-gui-l1-1-0 (introduced in Windows 8)
---

# LoadIconW function

## -description

Loads the specified icon resource from the executable (.exe) file associated with an application instance.

> [!NOTE]
> This function has been superseded by the [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew) function (with **LR_DEFAULTSIZE** and **LR_SHARED** flags set).

## -parameters

### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the module of either a DLL or executable (.exe) file that contains the icon to be loaded. For more information, see <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea">GetModuleHandle</a>.

To load a predefined system icon, set this parameter to <b>NULL</b>.

### -param lpIconName [in]

Type: <b>LPCTSTR</b>

If <i>hInstance</i> is non-<b>NULL</b>, <i>lpIconName</i> specifies the icon resource either by name or ordinal. This ordinal must be packaged by using the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcew">MAKEINTRESOURCE</a> macro.

If <i>hInstance</i> is <b>NULL</b>, <i>lpIconName</i> specifies the [identifier (beginning with the IDI\_ prefix)](/windows/win32/menurc/about-icons) of a predefined system icon to load.

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the newly loaded icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>LoadIcon</b> loads the icon resource only if it has not been loaded; otherwise, it retrieves a handle to the existing resource. The function searches the icon resource for the icon most appropriate for the current display. The icon resource can be a color or monochrome bitmap. 

<b>LoadIcon</b> can only load an icon whose size conforms to the <b>SM_CXICON</b> and <b>SM_CYICON</b> system metric values. Use the <a href="/windows/desktop/api/winuser/nf-winuser-loadimagew">LoadImage</a> function to load icons of other sizes.

> [!NOTE]
> The winuser.h header defines LoadIcon as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-createicon">CreateIcon</a>

<a href="/windows/desktop/menurc/icons">Icons</a>

<a href="/windows/desktop/api/winuser/nf-winuser-loadimagew">LoadImage</a>

<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>

<a href="/windows/win32/api/winuser/nf-winuser-is_intresource">IS_INTRESOURCE</a>
