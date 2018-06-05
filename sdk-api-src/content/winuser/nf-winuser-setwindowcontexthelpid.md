---
UID: NF:winuser.SetWindowContextHelpId
title: SetWindowContextHelpId function
author: windows-sdk-content
description: Associates a Help context identifier with the specified window.
old-location: shell\SetWindowContextHelpId.htm
old-project: shell
ms.assetid: 7e0963d1-5807-4db5-9abf-cdb21a03b525
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SetWindowContextHelpId, SetWindowContextHelpId function [Windows Shell], _win32_SetWindowContextHelpId, shell.SetWindowContextHelpId, winuser/SetWindowContextHelpId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	SetWindowContextHelpId
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetWindowContextHelpId function


## -description


Associates a Help context identifier with the specified window.


## -parameters




### -param

TBD




#### - dwContextHelpId

Type: <b>DWORD</b>

The Help context identifier.


#### - hwnd

Type: <b>HWND</b>

A handle to the window with which to associate the Help context identifier.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.

To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a child window does not have a Help context identifier, it inherits the identifier of its parent window. Likewise, if an owned window does not have a Help context identifier, it inherits the identifier of its owner window. This inheritance of Help context identifiers allows an application to set just one identifier for a dialog box and all of its controls.




## -see-also




<a href="https://msdn.microsoft.com/28e57c01-0327-4f64-9ef4-ca13c3c32b0c">GetWindowContextHelpId</a>
 

 

