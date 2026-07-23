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
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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

To specify a desired height or width, use the [CreateIconFromResourceEx](/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex) function.

## -parameters

### -param presbits [in]

Type: **PBYTE**

The buffer pointer containing the icon or cursor resource bits. These bits are typically loaded by calls to the [LookupIconIdFromDirectory](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory), [LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex), and [LoadResource](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) functions.

See [Cursor and Icon Resources](/windows/win32/menurc/resource-file-formats#cursor-and-icon-resources) for more info on icon and cursor resource format.

### -param dwResSize [in]

Type: **DWORD**

The size, in bytes, of the set of bits pointed to by the *presbits* parameter.

### -param fIcon [in]

Type: **BOOL**

Indicates whether an icon or a cursor is to be created. If this parameter is **TRUE**, an icon is to be created. If it is **FALSE**, a cursor is to be created.

The [LOCALHEADER](/windows/win32/menurc/localheader) structure defines cursor hotspot and is the first data read from the cursor resource bits.

### -param dwVer [in]

Type: **DWORD**

The version number of the icon or cursor format for the resource bits pointed to by the *presbits* parameter. The value must be greater than or equal to 0x00020000 and less than or equal to 0x00030000. This parameter is generally set to 0x00030000.

## -returns

Type: **HICON**

If the function succeeds, the return value is a handle to the icon or cursor.

If the function fails, the return value is **NULL**. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The **CreateIconFromResource**, [CreateIconFromResourceEx](/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex), [CreateIconIndirect](/windows/desktop/api/winuser/nf-winuser-createiconindirect), [GetIconInfo](/windows/desktop/api/winuser/nf-winuser-geticoninfo), [LookupIconIdFromDirectory](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory), and [LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex) functions allow shell applications and icon browsers to examine and use resources throughout the system.

The **CreateIconFromResource** function calls [CreateIconFromResourceEx](/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex) passing `LR_DEFAULTSIZE|LR_SHARED` as flags.

You should call [DestroyIcon](/windows/win32/api/winuser/nf-winuser-destroyicon) for icons or [DestroyCursor](/windows/win32/api/winuser/nf-winuser-destroycursor) for cursors created with **CreateIconFromResource**.

## -see-also

[CreateIconFromResourceEx](/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex)

[CreateIconIndirect](/windows/desktop/api/winuser/nf-winuser-createiconindirect)

[GetIconInfo](/windows/desktop/api/winuser/nf-winuser-geticoninfo)

[Icons](/windows/desktop/menurc/icons)

[LoadResource](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource)

[LookupIconIdFromDirectory](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory)

[LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex)
