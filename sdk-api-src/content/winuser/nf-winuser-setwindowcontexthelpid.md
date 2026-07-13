---
UID: NF:winuser.SetWindowContextHelpId
title: SetWindowContextHelpId function (winuser.h)
description: Associates a Help context identifier with the specified window.
helpviewer_keywords: ["SetWindowContextHelpId","SetWindowContextHelpId function [Windows Shell]","_win32_SetWindowContextHelpId","shell.SetWindowContextHelpId","winuser/SetWindowContextHelpId"]
old-location: shell\SetWindowContextHelpId.htm
tech.root: shell
ms.assetid: 7e0963d1-5807-4db5-9abf-cdb21a03b525
ms.date: 12/05/2018
ms.keywords: SetWindowContextHelpId, SetWindowContextHelpId function [Windows Shell], _win32_SetWindowContextHelpId, shell.SetWindowContextHelpId, winuser/SetWindowContextHelpId
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - SetWindowContextHelpId
 - winuser/SetWindowContextHelpId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - ext-ms-win-ntuser-misc-l1-5-1.dll
 - ext-ms-win-ntuser-misc-l1-5-0.dll
 - ext-ms-win-ntuser-misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-2-0.dll
 - ext-ms-win-ntuser-misc-l1-1-0.dll
 - User32.dll
api_name:
 - SetWindowContextHelpId
---

# SetWindowContextHelpId function


## -description

Associates a Help context identifier with the specified window.

## -parameters

### -param unnamedParam1

Type: <b>HWND</b>

A handle to the window with which to associate the Help context identifier.

### -param unnamedParam2

Type: <b>DWORD</b>

The Help context identifier.

## -returns

Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a child window does not have a Help context identifier, it inherits the identifier of its parent window. Likewise, if an owned window does not have a Help context identifier, it inherits the identifier of its owner window. This inheritance of Help context identifiers allows an application to set just one identifier for a dialog box and all of its controls.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getwindowcontexthelpid">GetWindowContextHelpId</a>