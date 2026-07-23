---
UID: NF:winuser.CreateIconFromResourceEx
title: CreateIconFromResourceEx function (winuser.h)
description: Creates an icon or cursor from resource bits describing the icon. (CreateIconFromResourceEx)
helpviewer_keywords: ["CreateIconFromResourceEx","CreateIconFromResourceEx function [Menus and Other Resources]","LR_DEFAULTCOLOR","LR_DEFAULTSIZE","LR_MONOCHROME","_win32_CreateIconFromResourceEx","_win32_createiconfromresourceex_cpp","menurc.createiconfromresourceex","winui._win32_createiconfromresourceex","winuser/CreateIconFromResourceEx"]
old-location: menurc\createiconfromresourceex.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createiconfromresourceex.htm
ms.date: 12/05/2018
ms.keywords: CreateIconFromResourceEx, CreateIconFromResourceEx function [Menus and Other Resources], LR_DEFAULTCOLOR, LR_DEFAULTSIZE, LR_MONOCHROME, _win32_CreateIconFromResourceEx, _win32_createiconfromresourceex_cpp, menurc.createiconfromresourceex, winui._win32_createiconfromresourceex, winuser/CreateIconFromResourceEx
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
 - CreateIconFromResourceEx
 - winuser/CreateIconFromResourceEx
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
 - CreateIconFromResourceEx
---

# CreateIconFromResourceEx function


## -description

Creates an icon or cursor from resource bits describing the icon.

## -parameters

### -param presbits [in]

Type: **PBYTE**

A pointer to the buffer containing the image bits. These bits are typically loaded by calls to the [LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex) and [LoadResource](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) functions. For the buffer formats this function accepts, see the Remarks section.

See [Cursor and Icon Resources](/windows/win32/menurc/resource-file-formats#cursor-and-icon-resources) for more info on icon and cursor resource format.

### -param dwResSize [in]

Type: **DWORD**

The size, in bytes, of the set of bits pointed to by the *pbIconBits* parameter.

### -param fIcon [in]

Type: **BOOL**

Indicates whether an icon or a cursor is to be created. If this parameter is **TRUE**, an icon is to be created. If it is **FALSE**, a cursor is to be created.

### -param dwVer [in]

Type: **DWORD**

The version number of the icon or cursor format for the resource bits pointed to by the *presbits* parameter. The value must be greater than or equal to 0x00020000 and less than or equal to 0x00030000. This parameter is generally set to 0x00030000.

### -param cxDesired [in]

Type: **int**

The width, in pixels, of the icon or cursor. If this parameter is zero and the *Flags* parameter is **LR_DEFAULTSIZE**, the function uses the **SM_CXICON** or **SM_CXCURSOR** system metric value to set the width. If this parameter is zero and **LR_DEFAULTSIZE** is not used, the function creates the icon or cursor at the width stored in *presbits*, without scaling.

### -param cyDesired [in]

Type: **int**

The height, in pixels, of the icon or cursor. If this parameter is zero and the *Flags* parameter is **LR_DEFAULTSIZE**, the function uses the **SM_CYICON** or **SM_CYCURSOR** system metric value to set the height. If this parameter is zero and **LR_DEFAULTSIZE** is not used, the function creates the icon or cursor at the height stored in *presbits*, without scaling.

### -param Flags [in]

Type: **UINT**

A combination of the following values.

| Value | Meaning |
|---|---|
| **LR_DEFAULTCOLOR** 0x00000000 | Uses the default color format. |
| **LR_DEFAULTSIZE** 0x00000040 | Uses the width or height specified by the system metric values for cursors or icons, if the *cxDesired* or *cyDesired* values are set to zero. If this flag is not specified and *cxDesired* and *cyDesired* are set to zero, the function uses the actual resource size. |
| **LR_MONOCHROME** 0x00000001 | Creates a monochrome icon or cursor. |

## -returns

Type: **HICON**

If the function succeeds, the return value is a handle to the icon or cursor.

If the function fails, the return value is **NULL**. To get extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The *presbits* buffer holds a single icon (**RT_ICON**) or cursor (**RT_CURSOR**) image — not an icon or cursor resource group directory. Several buffer formats are accepted:

-   **A device-independent bitmap (DIB) image.** The image data begins with a [BITMAPINFOHEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader); other header versions are not accepted. For a cursor (*fIcon* = **FALSE**), the image is preceded by the cursor hotspot ([LOCALHEADER](/windows/win32/menurc/localheader)).
-   **A PNG image.** Pass the raw bytes of a PNG file to create an icon directly from PNG data without first writing it to a file. This is supported only for icons (*fIcon* = **TRUE**).
-   **A complete animated cursor or animated icon** — the contents of an `.ani` file (RIFF/ACON data). This is the same data stored in a module's animated-cursor (**RT_ANICURSOR**) or animated-icon (**RT_ANIICON**) resource. When *cxDesired* and *cyDesired* are zero and **LR_DEFAULTSIZE** is not used, the icon or cursor is created at the first size stored in the animation, without scaling. For this format, *fIcon* is ignored; the result type (icon or cursor) is determined by the animation data itself.

For all formats, *cxDesired*, *cyDesired*, and **LR_DEFAULTSIZE** select the image size as described for those parameters.

You should call [DestroyIcon](/windows/win32/api/winuser/nf-winuser-destroyicon) for icons or [DestroyCursor](/windows/win32/api/winuser/nf-winuser-destroycursor) for cursors created with **CreateIconFromResourceEx**.

#### Examples

For an example, see [Sharing Icon Resources](/windows/desktop/menurc/using-icons#sharing-icon-resources).

## -see-also

[BITMAPINFOHEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)

[CreateIconFromResource](/windows/desktop/api/winuser/nf-winuser-createiconfromresource)

[CreateIconIndirect](/windows/desktop/api/winuser/nf-winuser-createiconindirect)

[DestroyIcon](/windows/desktop/api/winuser/nf-winuser-destroyicon)

[GetIconInfo](/windows/desktop/api/winuser/nf-winuser-geticoninfo)

[Icons](/windows/desktop/menurc/icons)

[LoadResource](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource)

[LookupIconIdFromDirectoryEx](/windows/desktop/api/winuser/nf-winuser-lookupiconidfromdirectoryex)
