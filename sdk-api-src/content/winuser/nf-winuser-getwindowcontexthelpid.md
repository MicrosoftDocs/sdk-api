---
UID: NF:winuser.GetWindowContextHelpId
title: GetWindowContextHelpId function (winuser.h)
description: Retrieves the Help context identifier, if any, associated with the specified window.helpviewer_keywords: ["GetWindowContextHelpId","GetWindowContextHelpId function [Windows Shell]","_win32_GetWindowContextHelpId","shell.GetWindowContextHelpId","winuser/GetWindowContextHelpId"]
old-location: shell\GetWindowContextHelpId.htm
tech.root: shell
ms.assetid: 28e57c01-0327-4f64-9ef4-ca13c3c32b0c
ms.date: 12/05/2018
ms.keywords: GetWindowContextHelpId, GetWindowContextHelpId function [Windows Shell], _win32_GetWindowContextHelpId, shell.GetWindowContextHelpId, winuser/GetWindowContextHelpId
f1_keywords:
- winuser/GetWindowContextHelpId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- User32.dll
api_name:
- GetWindowContextHelpId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetWindowContextHelpId function


## -description


Retrieves the Help context identifier, if any, associated with the specified window.


## -parameters




### -param Arg1

Type: <b>HWND</b>

A handle to the window for which the Help context identifier is to be retrieved.


## -returns



Type: <b>DWORD</b>

Returns the Help context identifier if the window has one, or zero otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowcontexthelpid">SetWindowContextHelpId</a>
 

 

