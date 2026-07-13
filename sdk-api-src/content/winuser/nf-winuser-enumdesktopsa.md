---
UID: NF:winuser.EnumDesktopsA
title: EnumDesktopsA function (winuser.h)
description: Enumerates all desktops associated with the specified window station of the calling process. The function passes the name of each desktop, in turn, to an application-defined callback function. (ANSI)
helpviewer_keywords: ["EnumDesktopsA", "winuser/EnumDesktopsA"]
old-location: winstation\enumdesktops.htm
tech.root: winstation
ms.assetid: 3e900b34-2c60-4281-881f-13a746674aec
ms.date: 12/05/2018
ms.keywords: EnumDesktops, EnumDesktops function [Windows Stations and Desktops], EnumDesktopsA, EnumDesktopsW, _win32_enumdesktops, base.enumdesktops, winstation.enumdesktops, winuser/EnumDesktops, winuser/EnumDesktopsA, winuser/EnumDesktopsW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumDesktopsA
 - winuser/EnumDesktopsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-windowstation-ansi-l1-1-1.dll
 - ext-ms-win-ntuser-windowstation-ansi-l1-1-0.dll
 - User32.dll
api_name:
 - EnumDesktops
 - EnumDesktopsA
 - EnumDesktopsW
---

# EnumDesktopsA function


## -description

Enumerates all desktops associated with the specified window station of the calling process. The function passes the name of each desktop, in turn, to an application-defined callback function.

## -parameters

### -param hwinsta [in, optional]

A handle to the window station whose desktops are to be enumerated. This handle is returned by the 
<a href="/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a>, or 
<a href="/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a> function, and must have the WINSTA_ENUMDESKTOPS access right. For more information, see 
<a href="/windows/desktop/winstation/window-station-security-and-access-rights">Window Station Security and Access Rights</a>.

If this parameter is NULL, the current window station is used.

### -param lpEnumFunc [in]

A pointer to an application-defined 
<a href="/previous-versions/windows/desktop/legacy/ms682612(v=vs.85)">EnumDesktopProc</a> callback function.

### -param lParam [in]

An application-defined value to be passed to the callback function.

## -returns

If the function succeeds, it returns the  nonzero value returned by the callback function that was pointed to by <i>lpEnumFunc</i>.

If the function is unable to perform the enumeration, the return value is zero. Call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

If the callback function fails, the return value is zero. The callback function can  call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to set an error code for the caller to retrieve by calling <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>EnumDesktops</b> function enumerates only those desktops for which the calling process has the DESKTOP_ENUMERATE access right. For more information, see 
<a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>.

The 
<b>EnumDesktops</b> function repeatedly invokes the <i>lpEnumFunc</i> callback function until the last desktop is enumerated or the callback function returns FALSE.





> [!NOTE]
> The winuser.h header defines EnumDesktops as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/previous-versions/windows/desktop/legacy/ms682612(v=vs.85)">EnumDesktopProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation">GetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
