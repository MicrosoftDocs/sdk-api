---
UID: NF:winuser.CopyIcon
title: CopyIcon function (winuser.h)
description: Copies the specified icon from another module to the current module.
helpviewer_keywords: ["CopyIcon","CopyIcon function [Menus and Other Resources]","_win32_CopyIcon","_win32_copyicon_cpp","menurc.copyicon","winui._win32_copyicon","winuser/CopyIcon"]
old-location: menurc\copyicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\copyicon.htm
ms.date: 12/05/2018
ms.keywords: CopyIcon, CopyIcon function [Menus and Other Resources], _win32_CopyIcon, _win32_copyicon_cpp, menurc.copyicon, winui._win32_copyicon, winuser/CopyIcon
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
 - CopyIcon
 - winuser/CopyIcon
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
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - CopyIcon
req.apiset: ext-ms-win-ntuser-gui-l1-3-0 (introduced in Windows 10, version 10.0.10240)
---

# CopyIcon function


## -description

Copies the specified icon from another module to the current module.

## -parameters

### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon to be copied.

## -returns

Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the duplicate icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>CopyIcon</b> function enables an application or DLL to get its own handle to an icon owned by another module. If the other module is freed, the application icon will still be able to use the icon. 

Before closing, an application must call the <a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a> function to free any system resources associated with the icon.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-copycursor">CopyCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroyicon">DestroyIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-drawicon">DrawIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-drawiconex">DrawIconEx</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<b>Reference</b>
