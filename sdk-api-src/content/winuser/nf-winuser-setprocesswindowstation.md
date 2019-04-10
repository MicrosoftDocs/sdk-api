---
UID: NF:winuser.SetProcessWindowStation
title: SetProcessWindowStation function (winuser.h)
author: windows-sdk-content
description: Assigns the specified window station to the calling process.
old-location: winstation\setprocesswindowstation.htm
tech.root: winstation
ms.assetid: d64814a7-945c-4e73-a977-5f696d60610e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetProcessWindowStation, SetProcessWindowStation function [Windows Stations and Desktops], _win32_setprocesswindowstation, base.setprocesswindowstation, winstation.setprocesswindowstation, winuser/SetProcessWindowStation
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-WindowStation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - SetProcessWindowStation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetProcessWindowStation function


## -description


Assigns the specified window station to the calling process. This enables the process to access objects in the window station such as desktops, the clipboard, and global atoms. All subsequent operations on the window station use the access rights granted to <i>hWinSta</i>.


## -parameters




### -param hWinSta [in]

A handle to the window station. This can be a handle returned by the 
<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>, 
<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>, or 
<a href="https://msdn.microsoft.com/f8929122-d277-4260-b2a7-5e76eb3ca876">GetProcessWindowStation</a> function.

This window station must be associated with the current session.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a>



<a href="https://msdn.microsoft.com/f8929122-d277-4260-b2a7-5e76eb3ca876">GetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>



<a href="https://msdn.microsoft.com/619c591f-54b7-4b61-aa07-fc57e05ee37a">SetThreadDesktop</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>



<a href="https://msdn.microsoft.com/617661e2-3b0d-42a9-9769-2ba0957c31a8">Window Stations</a>
 

 

