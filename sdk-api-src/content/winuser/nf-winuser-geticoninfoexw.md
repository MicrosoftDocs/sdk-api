---
UID: NF:winuser.GetIconInfoExW
title: GetIconInfoExW function (winuser.h)
description: Retrieves information about the specified icon or cursor. GetIconInfoEx extends GetIconInfo by using the newer ICONINFOEX structure. (Unicode)
helpviewer_keywords: ["GetIconInfoEx", "GetIconInfoEx function [Menus and Other Resources]", "GetIconInfoExW", "_win32_GetIconInfoEx", "_win32_geticoninfoex_cpp", "menurc.geticoninfoex", "winui._win32_geticoninfoex", "winuser/GetIconInfoEx", "winuser/GetIconInfoExW"]
old-location: menurc\geticoninfoex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\geticoninfoex.htm
ms.date: 12/05/2018
ms.keywords: GetIconInfoEx, GetIconInfoEx function [Menus and Other Resources], GetIconInfoExA, GetIconInfoExW, _win32_GetIconInfoEx, _win32_geticoninfoex_cpp, menurc.geticoninfoex, winui._win32_geticoninfoex, winuser/GetIconInfoEx, winuser/GetIconInfoExA, winuser/GetIconInfoExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetIconInfoExW (Unicode) and GetIconInfoExA (ANSI)
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
 - GetIconInfoExW
 - winuser/GetIconInfoExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - ext-ms-win-ntuser-gui-l1-3-0.dll
 - ext-ms-win-ntuser-gui-l1-2-0.dll
 - ext-ms-win-ntuser-gui-l1-1-1.dll
 - ext-ms-win-ntuser-gui-l1-1-0.dll
 - User32.dll
api_name:
 - GetIconInfoEx
 - GetIconInfoExA
 - GetIconInfoExW
---

# GetIconInfoExW function


## -description

Retrieves information about the specified icon or cursor. <b>GetIconInfoEx</b> extends <a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a> by using the newer <a href="/windows/desktop/api/winuser/ns-winuser-iconinfoexa">ICONINFOEX</a> structure.

## -parameters

### -param hicon [in]

Type: <b>HICON</b>

A handle to the icon or cursor.

To retrieve information about a standard icon or cursor, specify the [identifier beginning with the IDI\_ prefix](/windows/win32/menurc/about-icons) or the [identifier beginning with the IDC\_ prefix](/windows/win32/menurc/about-cursors) in this parameter.

### -param piconinfo [in, out]

Type: <b>PICONINFOEX</b>

When this method returns, contains a pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-iconinfoexa">ICONINFOEX</a> structure. The function fills in the structure's members.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> indicates success, <b>FALSE</b> indicates failure.

## -remarks

<b>GetIconInfoEx</b> creates bitmaps for the <b>hbmMask</b> and <b>hbmColor</b> or members of <a href="/windows/desktop/api/winuser/ns-winuser-iconinfoexw">ICONINFOEX</a>. The calling application must manage these bitmaps and delete them with <a href="/windows/win32/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> call when they are no longer necessary.

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The output returned is not affected by the DPI of the calling thread.

> [!NOTE]
> The winuser.h header defines GetIconInfoEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

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
