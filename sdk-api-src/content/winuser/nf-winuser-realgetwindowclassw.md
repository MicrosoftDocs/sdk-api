---
UID: NF:winuser.RealGetWindowClassW
title: RealGetWindowClassW function
author: windows-sdk-content
description: Retrieves a string that specifies the window type.
old-location: winmsg\realgetwindowclass.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\realgetwindowclass.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RealGetWindowClass, RealGetWindowClass function [Windows and Messages], RealGetWindowClassW, _win32_RealGetWindowClass, _win32_realgetwindowclass_cpp, winmsg.realgetwindowclass, winui._win32_realgetwindowclass, winuser/RealGetWindowClass, winuser/RealGetWindowClassW
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
req.unicode-ansi: RealGetWindowClassW (Unicode)
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
 - Ext-MS-Win-NTUser-Windowclass-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-windowclass-l1-1-2.dll
api_name:
 - RealGetWindowClass
 - RealGetWindowClassW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RealGetWindowClassW function


## -description


Retrieves a string that specifies the window type.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window whose type will be retrieved. 


### -param ptszClassName [out]

Type: <b>LPTSTR</b>

A pointer to a string that receives the window type. 


### -param cchClassNameMax [in]

Type: <b>UINT</b>

The length, in characters, of the buffer pointed to by the <i>pszType</i> parameter. 


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

If the function succeeds, the return value is the number of characters copied to the specified buffer. 

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows Overview</a>
 

 

