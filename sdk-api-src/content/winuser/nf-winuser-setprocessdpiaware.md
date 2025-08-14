---
UID: NF:winuser.SetProcessDPIAware
title: SetProcessDPIAware function (winuser.h)
description: SetProcessDPIAware may be altered or unavailable. Instead, use SetProcessDPIAwareness.
helpviewer_keywords: ["SetProcessDPIAware","SetProcessDPIAware function [Windows and Messages]","_win32_SetProcessDPIAware","_win32_setprocessdpiaware_cpp","winmsg.setprocessdpiaware","winui._win32_setprocessdpiaware","winuser/SetProcessDPIAware"]
old-location: winmsg\setprocessdpiaware.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setprocessdpiaware.htm
ms.date: 12/05/2018
ms.keywords: SetProcessDPIAware, SetProcessDPIAware function [Windows and Messages], _win32_SetProcessDPIAware, _win32_setprocessdpiaware_cpp, winmsg.setprocessdpiaware, winui._win32_setprocessdpiaware, winuser/SetProcessDPIAware
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - SetProcessDPIAware
 - winuser/SetProcessDPIAware
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-2.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-1.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-0.dll
 - ext-ms-win-rtcore-ntuser-dpi-l1-1-0.dll
 - User32.dll
 - Ext-MS-Win-RTCore-NTUser-sysparams-l1-1-0.dll
 - minuser.dll
api_name:
 - SetProcessDPIAware
---

# SetProcessDPIAware function


## -description

Sets the process-default DPI awareness to system-DPI awareness. This is equivalent to calling <a href="/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext">SetProcessDpiAwarenessContext</a> with a <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> value of DPI_AWARENESS_CONTEXT_SYSTEM_AWARE.

> [!NOTE]
> It is recommended that you set the process-default DPI awareness via application manifest, not an API call. See <a href="/windows/win32/hidpi/setting-the-default-dpi-awareness-for-a-process">Setting the default DPI awareness for a process</a> for more information. Setting the process-default DPI awareness via API call can lead to unexpected application behavior.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero. Otherwise, the return value is zero.

## -remarks

For more information, see <a href="/windows/win32/hidpi/setting-the-default-dpi-awareness-for-a-process">Setting the default DPI awareness for a process</a>.

## -see-also

<a href="/windows/win32/hidpi/setting-the-default-dpi-awareness-for-a-process">Setting the default DPI awareness for a process</a>
