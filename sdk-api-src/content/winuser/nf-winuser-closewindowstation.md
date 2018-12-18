---
UID: NF:winuser.CloseWindowStation
title: CloseWindowStation function
author: windows-sdk-content
description: Closes an open window station handle.
old-location: winstation\closewindowstation.htm
tech.root: winstation
ms.assetid: 417cb01b-c206-4b5b-9516-94e5d90717f4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CloseWindowStation, CloseWindowStation function [Windows Stations and Desktops], _win32_closewindowstation, base.closewindowstation, winstation.closewindowstation, winuser/CloseWindowStation
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
 - Ext-MS-Win-NTUser-Windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-l1-1-1.dll
 - api-ms-win-rtcore-ntuser-windowstation-l1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - CloseWindowStation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CloseWindowStation function


## -description


Closes an open window station handle.


## -parameters




### -param hWinSta [in]

A handle to the window station to be closed. This handle is returned by the 
<a href="https://msdn.microsoft.com/c1aee546-decd-46c9-8d02-d6792f5a6a0d">CreateWindowStation</a> or 
<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a> function. Do not specify the handle returned by the <a href="https://msdn.microsoft.com/f8929122-d277-4260-b2a7-5e76eb3ca876">GetProcessWindowStation</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<b>Windows Server 2003 and Windows XP/2000:  </b>This function does not set the last error code on failure.




## -remarks



The 
<b>CloseWindowStation</b> function will fail if the handle being closed is for the window station assigned to the calling process.




## -see-also




<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>



<a href="https://msdn.microsoft.com/617661e2-3b0d-42a9-9769-2ba0957c31a8">Window Stations</a>
 

 

