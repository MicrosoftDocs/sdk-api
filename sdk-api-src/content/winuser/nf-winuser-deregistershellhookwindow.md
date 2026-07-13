---
UID: NF:winuser.DeregisterShellHookWindow
title: DeregisterShellHookWindow function (winuser.h)
description: Unregisters a specified Shell window that is registered to receive Shell hook messages.
helpviewer_keywords: ["DeregisterShellHookWindow","DeregisterShellHookWindow function [Windows and Messages]","_win32_DeregisterShellHookWindow","_win32_deregistershellhookwindow_cpp","winmsg.deregistershellhookwindow","winui._win32_deregistershellhookwindow","winuser/DeregisterShellHookWindow"]
old-location: winmsg\deregistershellhookwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookfunctions\deregistershellhookwindow.htm
ms.date: 12/05/2018
ms.keywords: DeregisterShellHookWindow, DeregisterShellHookWindow function [Windows and Messages], _win32_DeregisterShellHookWindow, _win32_deregistershellhookwindow_cpp, winmsg.deregistershellhookwindow, winui._win32_deregistershellhookwindow, winuser/DeregisterShellHookWindow
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeregisterShellHookWindow
 - winuser/DeregisterShellHookWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-iam-l1-1-2.dll
 - User32.dll
 - API-MS-Win-RTCore-NTUser-shell-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-iam-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-Iam-L1-1-1.dll
api_name:
 - DeregisterShellHookWindow
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
		<a href="/windows/desktop/api/winuser/nf-winuser-registershellhookwindow">RegisterShellHookWindow</a> function.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the function succeeds; <b>FALSE</b> if the
				function fails.

## -remarks

This function was not included in the SDK headers and libraries until Windows XP with Service Pack 1 (SP1) and Windows Server 2003. If you do not have a header file and import library for this function, you can call the function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registershellhookwindow">RegisterShellHookWindow</a>



<a href="/windows/desktop/winmsg/windows">Windows</a>