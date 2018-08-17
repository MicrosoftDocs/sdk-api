---
UID: NF:winuser.GetWindowModuleFileNameA
title: GetWindowModuleFileNameA function
author: windows-sdk-content
description: Retrieves the full path and file name of the module associated with the specified window handle.
old-location: winmsg\getwindowmodulefilename.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowmodulefilename.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetWindowModuleFileName, GetWindowModuleFileName function [Windows and Messages], GetWindowModuleFileNameA, GetWindowModuleFileNameW, _win32_GetWindowModuleFileName, _win32_getwindowmodulefilename_cpp, winmsg.getwindowmodulefilename, winui._win32_getwindowmodulefilename, winuser/GetWindowModuleFileName, winuser/GetWindowModuleFileNameA, winuser/GetWindowModuleFileNameW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



Type: <strong>Type: <b>UINT</b>
</strong>

The return value is the total number of characters copied into the buffer. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows Overview</a>
 

 

