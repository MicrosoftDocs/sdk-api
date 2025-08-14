---
UID: NF:winuser.CreateIconFromResource
title: CreateIconFromResource function (winuser.h)
description: Creates an icon or cursor from resource bits describing the icon. (CreateIconFromResource)
helpviewer_keywords: ["CreateIconFromResource","CreateIconFromResource function [Menus and Other Resources]","_win32_CreateIconFromResource","_win32_createiconfromresource_cpp","menurc.createiconfromresource","winui._win32_createiconfromresource","winuser/CreateIconFromResource"]
old-location: menurc\createiconfromresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createiconfromresource.htm
ms.date: 12/05/2018
ms.keywords: CreateIconFromResource, CreateIconFromResource function [Menus and Other Resources], _win32_CreateIconFromResource, _win32_createiconfromresource_cpp, menurc.createiconfromresource, winui._win32_createiconfromresource, winuser/CreateIconFromResource
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
 - CreateIconFromResource
 - winuser/CreateIconFromResource
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
 - CreateIconFromResource
---

# CreateIconFromResource function


## -description

Creates an icon or cursor from resource bits describing the icon.

To specify a desired height or width, use the <a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a> function.

## -parameters

### -param presbits [in]

Type: <b>PBYTE</b>

The DWORD-aligned buffer pointer containing the icon or cursor resource bits. These bits are typically loaded by calls to the <a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory">LookupIconIdFromDirectory</a>, <a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a>, and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a> functions.

See <a href="/windows/win32/menurc/resource-file-formats#cursor-and-icon-resources">Cursor and Icon Resources</a> for more info on icon and cursor resource format.

### -param dwResSize [in]

Type: <b>DWORD</b>

The size, in bytes, of the set of bits pointed to by the <i>presbits</i> parameter.

### -param fIcon [in]

Type: <b>BOOL</b>

Indicates whether an icon or a cursor is to be created. If this parameter is <b>TRUE</b>, an icon is to be created. If it is <b>FALSE</b>, a cursor is to be created. 

The <a href="/windows/win32/menurc/localheader">LOCALHEADER</a> structure defines cursor hotspot and is the first data read from the cursor resource bits.

### -param dwVer [in]

Type: <b>DWORD</b>

The version number of the icon or cursor format for the resource bits pointed to by the <i>presbits</i> parameter. The value must be greater than or equal to 0x00020000 and less than or equal to 0x00030000. This parameter is generally set to 0x00030000.

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>CreateIconFromResource</b>, <a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a>, <a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>, <a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>, <a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory">LookupIconIdFromDirectory</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a> functions allow shell applications and icon browsers to examine and use resources throughout the system. 

The <b>CreateIconFromResource</b> function calls <a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a> passing <code>LR_DEFAULTSIZE|LR_SHARED</code> as flags.

You should call <a href="/windows/win32/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> for icons or <a href="/windows/win32/api/winuser/nf-winuser-destroycursor">DestroyCursor</a> for cursors created with <b>CreateIconFromResource</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource">LoadResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory">LookupIconIdFromDirectory</a>



<a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a>



<b>Reference</b>
