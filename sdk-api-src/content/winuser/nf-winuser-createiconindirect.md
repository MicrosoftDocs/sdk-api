---
UID: NF:winuser.CreateIconIndirect
title: CreateIconIndirect function (winuser.h)
description: Creates an icon or cursor from an ICONINFO structure.
helpviewer_keywords: ["CreateIconIndirect","CreateIconIndirect function [Menus and Other Resources]","_win32_CreateIconIndirect","_win32_createiconindirect_cpp","menurc.createiconindirect","winui._win32_createiconindirect","winuser/CreateIconIndirect"]
old-location: menurc\createiconindirect.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\createiconindirect.htm
ms.date: 12/05/2018
ms.keywords: CreateIconIndirect, CreateIconIndirect function [Menus and Other Resources], _win32_CreateIconIndirect, _win32_createiconindirect_cpp, menurc.createiconindirect, winui._win32_createiconindirect, winuser/CreateIconIndirect
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
 - CreateIconIndirect
 - winuser/CreateIconIndirect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-gui-l1-1-1.dll
 - ext-ms-win-ntuser-gui-l1-3-1.dll
 - User32.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - CreateIconIndirect
req.apiset: ext-ms-win-ntuser-gui-l1-3-0 (introduced in Windows 10, version 10.0.10240)
---

# CreateIconIndirect function


## -description

Creates an icon or cursor from an <a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a> structure.

## -parameters

### -param piconinfo [in]

Type: <b>PICONINFO</b>

A pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a> structure the function uses to create the icon or cursor.

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the icon or cursor that is created.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The system copies the bitmaps in the <a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a> structure before creating the icon or cursor. Because the system may temporarily select the bitmaps in a device context, the <b>hbmMask</b> and <b>hbmColor</b> members of the <b>ICONINFO</b> structure should not already be selected into a device context. The application must continue to manage the original bitmaps and delete them when they are no longer necessary. 

When you are finished using the icon, destroy it using the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function.

#### Examples

For an example, see <a href="/windows/win32/menurc/using-cursors#creating-a-cursor">Creating a Cursor</a>.

## -see-also

<b>Conceptual</b>

<a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>

<a href="/windows/desktop/api/winuser/ns-winuser-iconinfo">ICONINFO</a>

<a href="/windows/desktop/menurc/icons">Icons</a>
