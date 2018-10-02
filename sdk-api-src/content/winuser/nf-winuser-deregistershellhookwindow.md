---
UID: NF:winuser.DeregisterShellHookWindow
title: DeregisterShellHookWindow function
author: windows-sdk-content
description: Unregisters a specified Shell window that is registered to receive Shell hook messages.
old-location: winmsg\deregistershellhookwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\deregistershellhookwindow.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeregisterShellHookWindow, DeregisterShellHookWindow function [Windows and Messages], _win32_DeregisterShellHookWindow, _win32_deregistershellhookwindow_cpp, winmsg.deregistershellhookwindow, winui._win32_deregistershellhookwindow, winuser/DeregisterShellHookWindow
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
 - API-MS-Win-RTCore-NTUser-shell-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-iam-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-Iam-L1-1-1.dll
api_name:
 - DeregisterShellHookWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeregisterShellHookWindow function


## -description


<p class="CCE_Message">[This function is not intended for general
      use. It may
      be altered or unavailable in subsequent versions of Windows.]

Unregisters a specified Shell window that is registered to receive Shell
		hook messages.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window to be unregistered. The window was registered with a call to the
		<a href="https://msdn.microsoft.com/en-us/library/ms644989(v=VS.85).aspx">RegisterShellHookWindow</a> function.


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

<b>TRUE</b> if the function succeeds; <b>FALSE</b> if the
				function fails. 




## -remarks



This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644989(v=VS.85).aspx">RegisterShellHookWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632595(v=VS.85).aspx">Windows</a>
 

 

