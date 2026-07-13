---
UID: NF:winuser.SetUserObjectInformationW
title: SetUserObjectInformationW function (winuser.h)
description: Sets information about the specified window station or desktop object. (Unicode)
helpviewer_keywords: ["SetUserObjectInformation", "SetUserObjectInformation function [Windows Stations and Desktops]", "SetUserObjectInformationW", "UOI_FLAGS", "UOI_TIMERPROC_EXCEPTION_SUPPRESSION", "_win32_setuserobjectinformation", "base.setuserobjectinformation", "winstation.setuserobjectinformation", "winuser/SetUserObjectInformation", "winuser/SetUserObjectInformationW"]
old-location: winstation\setuserobjectinformation.htm
tech.root: winstation
ms.assetid: 42ce6946-1659-41a3-8ba7-21588583b4bd
ms.date: 12/05/2018
ms.keywords: SetUserObjectInformation, SetUserObjectInformation function [Windows Stations and Desktops], SetUserObjectInformationA, SetUserObjectInformationW, UOI_FLAGS, UOI_TIMERPROC_EXCEPTION_SUPPRESSION, _win32_setuserobjectinformation, base.setuserobjectinformation, winstation.setuserobjectinformation, winuser/SetUserObjectInformation, winuser/SetUserObjectInformationA, winuser/SetUserObjectInformationW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetUserObjectInformationW (Unicode) and SetUserObjectInformationA (ANSI)
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
 - SetUserObjectInformationW
 - winuser/SetUserObjectInformationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetUserObjectInformation
 - SetUserObjectInformationA
 - SetUserObjectInformationW
---

# SetUserObjectInformationW function


## -description

Sets information about the specified window station or desktop object.

## -parameters

### -param hObj [in]

A handle to the window station, desktop object or a current process pseudo handle. This handle can be returned by the  <a href="/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a>, 
<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>, <a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a> or  <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> function.

### -param nIndex [in]

The object information to be set. This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UOI_FLAGS"></a><a id="uoi_flags"></a><dl>
<dt><b>UOI_FLAGS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Sets the object's handle flags. The <i>pvInfo</i> parameter must point to a 
<a href="/windows/desktop/api/winuser/ns-winuser-userobjectflags">USEROBJECTFLAGS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="UOI_TIMERPROC_EXCEPTION_SUPPRESSION"></a><a id="uoi_timerproc_exception_suppression"></a><dl>
<dt><b>UOI_TIMERPROC_EXCEPTION_SUPPRESSION</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Sets the exception handling behavior when calling <a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a>.
 <i>hObj</i> must be the process handle returned by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> function.
 

The <i>pvInfo</i> parameter must point to a BOOL.  If TRUE, Windows will enclose its calls to <a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a> with an exception handler that consumes and discards all exceptions. This has been the default behavior since Windows 2000, although that may change in future versions of Windows.  

If <i>pvInfo</i>  points to FALSE, Windows will not enclose its calls to <a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a> with an exception handler. A setting of FALSE is recommended.  Otherwise, the application could behave unpredictably, and could be more vulnerable to security exploits.

</td>
</tr>
</table>

### -param pvInfo [in]

A pointer to a buffer containing the object information, or a BOOL.

### -param nLength [in]

The size of the information contained in the buffer pointed to by <i>pvInfo</i>, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowstationa">CreateWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa">GetUserObjectInformation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-opendesktopa">OpenDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openwindowstationa">OpenWindowStation</a>



<a href="/windows/desktop/api/winuser/ns-winuser-userobjectflags">USEROBJECTFLAGS</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>



<a href="/windows/desktop/winstation/window-stations">Window Stations</a>

## -remarks

> [!NOTE]
> The winuser.h header defines SetUserObjectInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
