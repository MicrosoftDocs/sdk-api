---
UID: NF:winuser.SetThreadDesktop
title: SetThreadDesktop function
author: windows-sdk-content
description: Assigns the specified desktop to the calling thread. All subsequent operations on the desktop use the access rights granted to the desktop.
old-location: winstation\setthreaddesktop.htm
tech.root: winstation
ms.assetid: 619c591f-54b7-4b61-aa07-fc57e05ee37a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SetThreadDesktop, SetThreadDesktop function [Windows Stations and Desktops], _win32_setthreaddesktop, base.setthreaddesktop, winstation.setthreaddesktop, winuser/SetThreadDesktop
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SetThreadDesktop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadDesktop function


## -description


Assigns the specified desktop to the calling thread. All subsequent operations on the desktop use the access rights granted to the desktop.


## -parameters




### -param hDesktop [in]

A handle to the desktop to be assigned to the calling thread. This handle is returned by the 
<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>, 
<a href="https://msdn.microsoft.com/51eec935-43c7-495b-b1fc-2bd5ba1e0090">GetThreadDesktop</a>, <a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>, or 
<a href="https://msdn.microsoft.com/023d421e-bf32-4e08-b5b3-b7b2ca6c4e00">OpenInputDesktop</a> function.

This desktop must be associated with the current window station for the process.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SetThreadDesktop</b> function will fail if the calling thread has any windows or hooks on its current desktop (unless the <i>hDesktop</i> parameter is a handle to the current desktop).

<div class="alert"><b>Warning</b>  There is a significant security risk for any service that opens a window on the interactive desktop. By opening a desktop window, a service makes itself vulnerable to attack from the logged-on user, whose application could send malicious messages to the service's desktop window and affect its ability to function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>



<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/51eec935-43c7-495b-b1fc-2bd5ba1e0090">GetThreadDesktop</a>



<a href="https://msdn.microsoft.com/7f805f47-1737-4f4b-a74a-9c1423b65f2c">OpenDesktop</a>



<a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

