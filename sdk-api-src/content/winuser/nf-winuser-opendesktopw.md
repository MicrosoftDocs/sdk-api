---
UID: NF:winuser.OpenDesktopW
title: OpenDesktopW function (winuser.h)
description: Opens the specified desktop object. (Unicode)
helpviewer_keywords: ["DF_ALLOWOTHERACCOUNTHOOK", "OpenDesktop", "OpenDesktop function [Windows Stations and Desktops]", "OpenDesktopW", "_win32_opendesktop", "base.opendesktop", "winstation.opendesktop", "winuser/OpenDesktop", "winuser/OpenDesktopW"]
old-location: winstation\opendesktop.htm
tech.root: winstation
ms.assetid: 7f805f47-1737-4f4b-a74a-9c1423b65f2c
ms.date: 12/05/2018
ms.keywords: DF_ALLOWOTHERACCOUNTHOOK, OpenDesktop, OpenDesktop function [Windows Stations and Desktops], OpenDesktopA, OpenDesktopW, _win32_opendesktop, base.opendesktop, winstation.opendesktop, winuser/OpenDesktop, winuser/OpenDesktopA, winuser/OpenDesktopW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenDesktopW (Unicode) and OpenDesktopA (ANSI)
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
 - OpenDesktopW
 - winuser/OpenDesktopW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-WindowStation-Ansi-L1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - OpenDesktop
 - OpenDesktopA
 - OpenDesktopW
req.apiset: ext-ms-win-ntuser-windowstation-ansi-l1-1-1 (introduced in Windows 10, version 10.0.14393)
---

# OpenDesktopW function


## -description

Opens the specified desktop object.

## -parameters

### -param lpszDesktop [in]

The name of the desktop to be opened. Desktop names are case-insensitive.

This desktop must belong to the current window station.

### -param dwFlags [in]

This parameter can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DF_ALLOWOTHERACCOUNTHOOK"></a><a id="df_allowotheraccounthook"></a><dl>
<dt><b>DF_ALLOWOTHERACCOUNTHOOK</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Allows processes running in other accounts on the desktop to set hooks in this process.

</td>
</tr>
</table>

### -param fInherit [in]

If this value is <b>TRUE</b>, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.

### -param dwDesiredAccess [in]

The access to the desktop. For a list of access rights, see 
<a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is a handle to the opened desktop. When you are finished using the handle, call the 
<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a> function to close it.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling process must have an associated window station, either assigned by the system at process creation time or set by the 
<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a> function.

If the <i>dwDesiredAccess</i> parameter specifies the <b>READ_CONTROL</b>, <b>WRITE_DAC</b>, or <b>WRITE_OWNER</b> standard access rights, you must also request the <b>DESKTOP_READOBJECTS</b> and <b>DESKTOP_WRITEOBJECTS</b> access rights.





> [!NOTE]
> The winuser.h header defines OpenDesktop as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/desktop/api/winuser/nf-winuser-openinputdesktop">OpenInputDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddesktop">SetThreadDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-switchdesktop">SwitchDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
