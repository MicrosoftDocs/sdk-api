---
UID: NF:winuser.GetProcessDefaultLayout
title: GetProcessDefaultLayout function (winuser.h)
description: Retrieves the default layout that is used when windows are created with no parent or owner.
helpviewer_keywords: ["GetProcessDefaultLayout","GetProcessDefaultLayout function [Windows and Messages]","_win32_GetProcessDefaultLayout","_win32_getprocessdefaultlayout_cpp","winmsg.getprocessdefaultlayout","winui._win32_getprocessdefaultlayout","winuser/GetProcessDefaultLayout"]
old-location: winmsg\getprocessdefaultlayout.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getprocessdefaultlayout.htm
ms.date: 12/05/2018
ms.keywords: GetProcessDefaultLayout, GetProcessDefaultLayout function [Windows and Messages], _win32_GetProcessDefaultLayout, _win32_getprocessdefaultlayout_cpp, winmsg.getprocessdefaultlayout, winui._win32_getprocessdefaultlayout, winuser/GetProcessDefaultLayout
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
 - GetProcessDefaultLayout
 - winuser/GetProcessDefaultLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetProcessDefaultLayout
req.apiset: ext-ms-win-ntuser-window-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# GetProcessDefaultLayout function


## -description

Retrieves the default layout that is used when windows are created with no parent or owner.

## -parameters

### -param pdwDefaultLayout [out]

Type: <b>DWORD*</b>

The current default process layout. For a list of values, see <a href="/windows/desktop/api/winuser/nf-winuser-setprocessdefaultlayout">SetProcessDefaultLayout</a>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The layout specifies how text and graphics are laid out in a window; the default is left to right. The <b>GetProcessDefaultLayout</b> function lets you know if the default layout has changed, from using <a href="/windows/desktop/api/winuser/nf-winuser-setprocessdefaultlayout">SetProcessDefaultLayout</a>.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocessdefaultlayout">SetProcessDefaultLayout</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>
