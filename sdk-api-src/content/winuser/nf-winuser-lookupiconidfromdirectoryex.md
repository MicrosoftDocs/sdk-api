---
UID: NF:winuser.LookupIconIdFromDirectoryEx
title: LookupIconIdFromDirectoryEx function (winuser.h)
description: Searches through icon or cursor data for the icon or cursor that best fits the current display device. (LookupIconIdFromDirectoryEx)
helpviewer_keywords: ["LR_DEFAULTCOLOR","LR_DEFAULTSIZE","LR_MONOCHROME","LookupIconIdFromDirectoryEx","LookupIconIdFromDirectoryEx function [Menus and Other Resources]","_win32_LookupIconIdFromDirectoryEx","_win32_lookupiconidfromdirectoryex_cpp","menurc.lookupiconidfromdirectoryex","winui._win32_lookupiconidfromdirectoryex","winuser/LookupIconIdFromDirectoryEx"]
old-location: menurc\lookupiconidfromdirectoryex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\lookupiconidfromdirectoryex.htm
ms.date: 12/05/2018
ms.keywords: LR_DEFAULTCOLOR, LR_DEFAULTSIZE, LR_MONOCHROME, LookupIconIdFromDirectoryEx, LookupIconIdFromDirectoryEx function [Menus and Other Resources], _win32_LookupIconIdFromDirectoryEx, _win32_lookupiconidfromdirectoryex_cpp, menurc.lookupiconidfromdirectoryex, winui._win32_lookupiconidfromdirectoryex, winuser/LookupIconIdFromDirectoryEx
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
 - LookupIconIdFromDirectoryEx
 - winuser/LookupIconIdFromDirectoryEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - LookupIconIdFromDirectoryEx
---

# LookupIconIdFromDirectoryEx function


## -description

Searches through icon (**RT_GROUP_ICON**) or cursor (**RT_GROUP_CURSOR**) resource data for the icon or cursor that best fits the current display device.

If the resource group contains more than one image, the function assigns each candidate a score measuring how far it departs from the target, and returns the entry with the lowest score (a score of zero is an exact match). The target is the requested width and height (or, when those are zero, the system-metric size — see *cxDesired*) together with the color depth of the current display device. The score is the sum of three terms:
-   the absolute difference in width, in pixels — doubled if the candidate is narrower than the target;
-   the absolute difference in height, in pixels — doubled if the candidate is shorter than the target;
-   the absolute difference in color depth, in bits per pixel — always doubled.

Because the width and height terms are doubled only when the candidate is undersized, an image smaller than the requested size scores worse than one larger by the same amount (reducing size is preferred over enlarging it). Because the color-depth term is always doubled, a closer match in color depth is preferred over an equally close match in size. When two candidates score equally, the one with the greater color depth is chosen; if they are still equal, the earlier entry in the directory wins.

## -parameters

### -param presbits [in]

Type: **PBYTE**

The icon or cursor directory data. Because this function does not validate the resource data, it causes a general protection (GP) fault or returns an undefined value if *presbits* is not pointing to valid resource data.

### -param fIcon [in]

Type: **BOOL**

Indicates whether an icon or a cursor is sought. If this parameter is **TRUE**, the function is searching for an icon; if the parameter is **FALSE**, the function is searching for a cursor.

### -param cxDesired [in]

Type: **int**

The desired width, in pixels, of the icon or cursor. If this parameter is zero, the width used depends on the **LR_DEFAULTSIZE** flag; see the *Flags* parameter.

### -param cyDesired [in]

Type: **int**

The desired height, in pixels, of the icon or cursor. If this parameter is zero, the height used depends on the **LR_DEFAULTSIZE** flag; see the *Flags* parameter.

### -param Flags [in]

Type: **UINT**

A combination of the following values.

| Value | Meaning |
|---|---|
| **LR_DEFAULTCOLOR** 0x00000000 | Uses the default color format. |
| **LR_DEFAULTSIZE** 0x00000040 | If *cxDesired* or *cyDesired* is zero, uses the **SM_CXICON**/**SM_CXCURSOR** or **SM_CYICON**/**SM_CYCURSOR** system-metric size for that dimension. If this flag is not specified and both are zero, size does not take part in the selection (see the selection criteria above). |
| **LR_MONOCHROME** 0x00000001 | Searches for a monochrome icon or cursor. |

## -returns

Type: **int**

If the function succeeds, the return value is an integer resource identifier for the icon (**RT_ICON**) or cursor (**RT_CURSOR**) that best fits the current display device.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

A resource file of type **RT_GROUP_ICON** (**RT_GROUP_CURSOR** indicates cursors) contains icon (or cursor) data in several device-dependent and device-independent formats. **LookupIconIdFromDirectoryEx** searches the resource file for the icon (or cursor) that best fits the current display device and returns its integer identifier. The [FindResource](/windows/desktop/api/winbase/nf-winbase-findresourcea) and [FindResourceEx](/windows/desktop/api/winbase/nf-winbase-findresourceexa) functions use the [MAKEINTRESOURCE](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro with this identifier to locate the resource in the module.

The icon directory is loaded from a resource file with resource type **RT_GROUP_ICON** (or **RT_GROUP_CURSOR** for cursors), and an integer resource name for the specific icon (**RT_ICON**) or cursor (**RT_CURSOR**) to be loaded. [LoadResource](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) and [CreateIconFromResourceEx](/windows/win32/api/winuser/nf-winuser-createiconfromresourceex) functions may be used to create a corresponding icon or cursor.

The [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadicona), [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagea), and [LoadCursor](/windows/desktop/api/winuser/nf-winuser-loadcursora) functions use this function to search the specified resource data for the icon or cursor that best fits the current display device. [LoadIconWithScaleDown](/windows/win32/api/commctrl/nf-commctrl-loadiconwithscaledown) uses alternative search criteria for a best fit.

#### Examples

For an example, see [Sharing Icon Resources](/windows/win32/menurc/using-icons#sharing-icon-resources).

## -see-also

[CreateIconFromResourceEx](/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex)

[CreateIconIndirect](/windows/desktop/api/winuser/nf-winuser-createiconindirect)

[FindResource](/windows/desktop/api/winbase/nf-winbase-findresourcea)

[FindResourceEx](/windows/desktop/api/winbase/nf-winbase-findresourceexa)

[GetIconInfo](/windows/desktop/api/winuser/nf-winuser-geticoninfo)

[Icons](/windows/desktop/menurc/icons)

[LoadCursor](/windows/desktop/api/winuser/nf-winuser-loadcursora)

[LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadicona)

[LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagea)

[LookupIconIdFromDirectory](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectory)

[MAKEINTRESOURCE](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
