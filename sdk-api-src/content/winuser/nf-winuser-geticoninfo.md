---
UID: NF:winuser.GetIconInfo
title: GetIconInfo function (winuser.h)
description: Retrieves information about the specified icon or cursor.
helpviewer_keywords: ["GetIconInfo","GetIconInfo function [Menus and Other Resources]","_win32_GetIconInfo","_win32_geticoninfo_cpp","menurc.geticoninfo","winui._win32_geticoninfo","winuser/GetIconInfo"]
old-location: menurc\geticoninfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\geticoninfo.htm
ms.date: 12/05/2018
ms.keywords: GetIconInfo, GetIconInfo function [Menus and Other Resources], _win32_GetIconInfo, _win32_geticoninfo_cpp, menurc.geticoninfo, winui._win32_geticoninfo, winuser/GetIconInfo
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
 - GetIconInfo
 - winuser/GetIconInfo
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
 - GetIconInfo
req.apiset: ext-ms-win-ntuser-gui-l1-1-0 (introduced in Windows 8)
---

# GetIconInfo function


## -description

Retrieves information about the specified icon or cursor.

## -parameters

### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon or cursor.

To retrieve information about a standard icon or cursor, specify the [identifier beginning with the IDI\_ prefix](/windows/win32/menurc/about-icons) or the [identifier beginning with the IDC\_ prefix](/windows/win32/menurc/about-cursors) in this parameter.

### -param piconinfo [out]

Type: <b>PICONINFO</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a> structure. The function fills in the structure's members.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero and the function fills in the members of the specified <a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a> structure.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>GetIconInfo</b> creates bitmaps for the <b>hbmMask</b> and <b>hbmColor</b> or members of <a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a>. The calling application must manage these bitmaps and delete them with <a href="/windows/win32/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> call when they are no longer necessary.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is not affected by the DPI of the calling thread.

## -see-also

<b>Conceptual</b>

<a href="/windows/win32/gdi/bitmaps">Bitmaps</a>

<a href="/windows/win32/menurc/icons">Icons</a>

<a href="/windows/win32/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>

<a href="/windows/win32/api/wingdi/nf-wingdi-getobject">GetObject</a>

<a href="/windows/win32/api/wingdi/ns-wingdi-bitmap">BITMAP</a>

<a href="/windows/win32/api/winuser/nf-winuser-createicon">CreateIcon</a>

<a href="/windows/win32/api/winuser/nf-winuser-createiconfromresource">CreateIconFromResource</a>

<a href="/windows/win32/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>

<a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>

<a href="/windows/win32/api/winuser/nf-winuser-drawicon">DrawIcon</a>

<a href="/windows/win32/api/winuser/nf-winuser-drawiconex">DrawIconEx</a>

<a href="/windows/win32/api/winuser/nf-winuser-loadicona">LoadIcon</a>

<a href="/windows/win32/api/winuser/nf-winuser-lookupiconidfromdirectory">LookupIconIdFromDirectory</a>

<a href="/windows/win32/api/winuser/ns-winuser-iconinfo">ICONINFO</a>
