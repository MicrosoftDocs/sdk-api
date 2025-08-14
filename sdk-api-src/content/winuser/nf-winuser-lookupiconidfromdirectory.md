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

Searches through icon (<b>RT_GROUP_ICON</b>) or cursor (<b>RT_GROUP_CURSOR</b>) resource data for the icon or cursor that best fits the current display device.

To specify a desired height or width, use the <a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a> function. This function calls it by passing zero in the <b>cxDesired</b>/<b>cyDesired</b> parameters.

## -parameters

### -param presbits [in]

Type: <b>PBYTE</b>

The icon or cursor directory data. Because this function does not validate the resource data, it causes a general protection (GP) fault or returns an undefined value if <i>presbits</i> is not pointing to valid resource data.

### -param fIcon [in]

Type: <b>BOOL</b>

Indicates whether an icon or a cursor is sought. If this parameter is <b>TRUE</b>, the function is searching for an icon; if the parameter is <b>FALSE</b>, the function is searching for a cursor.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is an integer resource identifier for the icon (<b>RT_ICON</b>) or cursor (<b>RT_CURSOR</b>) that best fits the current display device. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A resource file of type <b>RT_GROUP_ICON</b> (<b>RT_GROUP_CURSOR</b> indicates cursors) contains icon (or cursor) data in several device-dependent and device-independent formats. <b>LookupIconIdFromDirectory</b> searches the resource file for the icon (or cursor) that best fits the current display device and returns its integer identifier. The <a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a> and <a href="/windows/desktop/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a> functions use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro with this identifier to locate the resource in the module. 

The icon directory is loaded from a resource file with resource type <b>RT_GROUP_ICON</b> (or <b>RT_GROUP_CURSOR</b> for cursors), and an integer resource name for the specific icon to be loaded. <b>LookupIconIdFromDirectory</b> returns an integer identifier that is the resource name of the icon that best fits the current display device. 

The <a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>, <a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> functions use this function to search the specified resource data for the icon or cursor that best fits the current display device.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresource">CreateIconFromResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findresourcea">FindResource</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findresourceexa">FindResourceEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-geticoninfo">GetIconInfo</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex">LookupIconIdFromDirectoryEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a>



<b>Reference</b>
