---
UID: NF:winuser.GetWindowModuleFileNameA
title: GetWindowModuleFileNameA function (winuser.h)
description: Retrieves the full path and file name of the module associated with the specified window handle. (ANSI)
helpviewer_keywords: ["GetWindowModuleFileNameA", "winuser/GetWindowModuleFileNameA"]
old-location: winmsg\getwindowmodulefilename.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowmodulefilename.htm
ms.date: 12/05/2018
ms.keywords: GetWindowModuleFileName, GetWindowModuleFileName function [Windows and Messages], GetWindowModuleFileNameA, GetWindowModuleFileNameW, _win32_GetWindowModuleFileName, _win32_getwindowmodulefilename_cpp, winmsg.getwindowmodulefilename, winui._win32_getwindowmodulefilename, winuser/GetWindowModuleFileName, winuser/GetWindowModuleFileNameA, winuser/GetWindowModuleFileNameW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetWindowModuleFileNameW (Unicode) and GetWindowModuleFileNameA (ANSI)
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
 - GetWindowModuleFileNameA
 - winuser/GetWindowModuleFileNameA
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
 - GetWindowModuleFileName
 - GetWindowModuleFileNameA
 - GetWindowModuleFileNameW
---

# GetWindowModuleFileNameA function


## -description

Retrieves the full path and file name of the module associated with the specified window handle.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window whose module file name is to be retrieved.

### -param pszFileName [out]

Type: <b>LPTSTR</b>

The path and file name.

### -param cchFileNameMax [in]

Type: <b>UINT</b>

The maximum number of characters that can be copied into the <i>lpszFileName</i> buffer.

## -returns

Type: <b>UINT</b>

The return value is the total number of characters copied into the buffer.

## -see-also

<a href="/windows/desktop/winmsg/windows">Windows Overview</a>

## -remarks

> [!NOTE]
> The winuser.h header defines GetWindowModuleFileName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
