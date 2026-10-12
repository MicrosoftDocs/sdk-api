---
UID: NF:winuser.LookupIconIdFromDirectory
title: LookupIconIdFromDirectory function (winuser.h)
description: Searches through icon or cursor data for the icon or cursor that best fits the current display device. (LookupIconIdFromDirectory)
helpviewer_keywords: ["LookupIconIdFromDirectory","LookupIconIdFromDirectory function [Menus and Other Resources]","_win32_LookupIconIdFromDirectory","_win32_lookupiconidfromdirectory_cpp","menurc.lookupiconidfromdirectory","winui._win32_lookupiconidfromdirectory","winuser/LookupIconIdFromDirectory"]
old-location: menurc\lookupiconidfromdirectory.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\lookupiconidfromdirectory.htm
ms.date: 12/05/2018
ms.keywords: LookupIconIdFromDirectory, LookupIconIdFromDirectory function [Menus and Other Resources], _win32_LookupIconIdFromDirectory, _win32_lookupiconidfromdirectory_cpp, menurc.lookupiconidfromdirectory, winui._win32_lookupiconidfromdirectory, winuser/LookupIconIdFromDirectory
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
 - LookupIconIdFromDirectory
 - winuser/LookupIconIdFromDirectory
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
 - LookupIconIdFromDirectory
---

# LookupIconIdFromDirectory function


## -description

Searches through icon (**RT_GROUP_ICON**) or cursor (**RT_GROUP_CURSOR**) resource data for the icon or cursor that best fits the current display device.

To specify a desired height or width, use the [LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex) function. This function calls it passing zero for *cxDesired*, *cyDesired*, and *Flags*. Because no size is requested and **LR_DEFAULTSIZE** is not used, size does not take part in the selection; the image is chosen by color depth as described for [LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex).

## -parameters

### -param presbits [in]

Type: **PBYTE**

The icon or cursor directory data. Because this function does not validate the resource data, it causes a general protection (GP) fault or returns an undefined value if *presbits* is not pointing to valid resource data.

### -param fIcon [in]

Type: **BOOL**

Indicates whether an icon or a cursor is sought. If this parameter is **TRUE**, the function is searching for an icon; if the parameter is **FALSE**, the function is searching for a cursor.

## -returns

Type: **int**

If the function succeeds, the return value is an integer resource identifier for the icon (**RT_ICON**) or cursor (**RT_CURSOR**) that best fits the current display device.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

A resource file of type **RT_GROUP_ICON** (**RT_GROUP_CURSOR** indicates cursors) contains icon (or cursor) data in several device-dependent and device-independent formats. **LookupIconIdFromDirectory** searches the resource file for the icon (or cursor) that best fits the current display device and returns its integer identifier. The [FindResource](/windows/desktop/api/winbase/nf-winbase-findresourcea) and [FindResourceEx](/windows/desktop/api/winbase/nf-winbase-findresourceexa) functions use the [MAKEINTRESOURCE](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro with this identifier to locate the resource in the module.

The icon directory is loaded from a resource file with resource type **RT_GROUP_ICON** (or **RT_GROUP_CURSOR** for cursors), and an integer resource name for the specific icon to be loaded. **LookupIconIdFromDirectory** returns an integer identifier that is the resource name of the icon that best fits the current display device.

The [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadicona), [LoadCursor](/windows/desktop/api/winuser/nf-winuser-loadcursora), and [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagea) functions use this function to search the specified resource data for the icon or cursor that best fits the current display device.

## -see-also

[CreateIconFromResource](/windows/desktop/api/winuser/nf-winuser-createiconfromresource)

[CreateIconIndirect](/windows/desktop/api/winuser/nf-winuser-createiconindirect)

[FindResource](/windows/desktop/api/winbase/nf-winbase-findresourcea)

[FindResourceEx](/windows/desktop/api/winbase/nf-winbase-findresourceexa)

[GetIconInfo](/windows/desktop/api/winuser/nf-winuser-geticoninfo)

[Icons](/windows/desktop/menurc/icons)

[LoadCursor](/windows/desktop/api/winuser/nf-winuser-loadcursora)

[LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadicona)

[LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagea)

[LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex)

[MAKEINTRESOURCE](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
