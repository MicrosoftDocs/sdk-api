---
UID: NF:winuser.EnumDesktopsA
title: EnumDesktopsA function (winuser.h)
author: windows-sdk-content
description: Enumerates all desktops associated with the specified window station of the calling process. The function passes the name of each desktop, in turn, to an application-defined callback function.
old-location: winstation\enumdesktops.htm
tech.root: winstation
ms.assetid: 3e900b34-2c60-4281-881f-13a746674aec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumDesktops, EnumDesktops function [Windows Stations and Desktops], EnumDesktopsA, EnumDesktopsW, _win32_enumdesktops, base.enumdesktops, winstation.enumdesktops, winuser/EnumDesktops, winuser/EnumDesktopsA, winuser/EnumDesktopsW
ms.topic: function
f1_keywords: 
 - "winuser/EnumDesktops"
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumDesktopsW (Unicode) and EnumDesktopsA (ANSI)
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
api_name:
 - EnumDesktops
 - EnumDesktopsA
 - EnumDesktopsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnumDesktopsA function


## -description


Enumerates all desktops associated with the specified window station of the calling process. The function passes the name of each desktop, in turn, to an application-defined callback function.


## -parameters




### -param hwinsta [in, optional]

A handle to the window station whose desktops are to be enumerated. This handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a> function, and must have the WINSTA_ENUMDESKTOPS access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/winstation/window-station-security-and-access-rights">Window Station Security and Access Rights</a>.

If this parameter is NULL, the current window station is used.


### -param lpEnumFunc [in]

A pointer to an application-defined 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms682612(v=vs.85)">EnumDesktopProc</a> callback function.


### -param lParam [in]

An application-defined value to be passed to the callback function.


## -returns



If the function succeeds, it returns the  nonzero value returned by the callback function that was pointed to by <i>lpEnumFunc</i>.

If the function is unable to perform the enumeration, the return value is zero. Call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

If the callback function fails, the return value is zero. The callback function can  call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to set an error code for the caller to retrieve by calling <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<b>EnumDesktops</b> function enumerates only those desktops for which the calling process has the DESKTOP_ENUMERATE access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>.

The 
<b>EnumDesktops</b> function repeatedly invokes the <i>lpEnumFunc</i> callback function until the last desktop is enumerated or the callback function returns FALSE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>



<a href="https://docs.microsoft.com/windows/desktop/winstation/desktops">Desktops</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms682612(v=vs.85)">EnumDesktopProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a>



<a href="https://docs.microsoft.com/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
 

 

