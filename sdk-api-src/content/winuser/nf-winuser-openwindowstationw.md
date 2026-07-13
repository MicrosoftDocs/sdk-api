---
UID: NF:winuser.OpenWindowStationW
title: OpenWindowStationW function (winuser.h)
description: Opens the specified window station. (Unicode)
helpviewer_keywords: ["OpenWindowStation", "OpenWindowStation function [Windows Stations and Desktops]", "OpenWindowStationW", "_win32_openwindowstation", "base.openwindowstation", "winstation.openwindowstation", "winuser/OpenWindowStation", "winuser/OpenWindowStationW"]
old-location: winstation\openwindowstation.htm
tech.root: winstation
ms.assetid: 78ee7100-1bad-4c2d-b923-c5e67191bd41
ms.date: 12/05/2018
ms.keywords: OpenWindowStation, OpenWindowStation function [Windows Stations and Desktops], OpenWindowStationA, OpenWindowStationW, _win32_openwindowstation, base.openwindowstation, winstation.openwindowstation, winuser/OpenWindowStation, winuser/OpenWindowStationA, winuser/OpenWindowStationW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenWindowStationW (Unicode) and OpenWindowStationA (ANSI)
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
 - OpenWindowStationW
 - winuser/OpenWindowStationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-RTCore-NTUser-WindowStation-l1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-Ansi-L1-1-1.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - OpenWindowStation
 - OpenWindowStationA
 - OpenWindowStationW
req.apiset: ext-ms-win-ntuser-windowstation-ansi-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# OpenWindowStationW function


## -description

Opens the specified window station.

## -parameters

### -param lpszWinSta [in]

The name of the window station to be opened. Window station names are case-insensitive.

This window station must belong to the current session.

### -param fInherit [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.

### -param dwDesiredAccess [in]

The access to the window station. For a list of access rights, see 
<a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window Station Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is the handle to the specified window station.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After you are done with the handle, you must call 
<a href="/windows/desktop/api/winuser/nf-winuser-closewindowstation">CloseWindowStation</a> to free the handle.





> [!NOTE]
> The winuser.h header defines OpenWindowStation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closewindowstation">CloseWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-exitwindows">ExitWindows</a>



<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>



<a href="/windows/desktop/winstation/window-stations">Window Stations</a>
