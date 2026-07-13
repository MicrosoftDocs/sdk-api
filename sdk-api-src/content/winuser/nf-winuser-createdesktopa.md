---
UID: NF:winuser.CreateDesktopA
title: CreateDesktopA function (winuser.h)
description: Creates a new desktop, associates it with the current window station of the calling process, and assigns it to the calling thread. (ANSI)
helpviewer_keywords: ["CreateDesktopA", "DF_ALLOWOTHERACCOUNTHOOK", "winuser/CreateDesktopA"]
old-location: winstation\createdesktop.htm
tech.root: winstation
ms.assetid: c6ed40c5-13a9-4697-a727-730adc6a912d
ms.date: 12/05/2018
ms.keywords: CreateDesktop, CreateDesktop function [Windows Stations and Desktops], CreateDesktopA, CreateDesktopW, DF_ALLOWOTHERACCOUNTHOOK, _win32_createdesktop, base.createdesktop, winstation.createdesktop, winuser/CreateDesktop, winuser/CreateDesktopA, winuser/CreateDesktopW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateDesktopW (Unicode) and CreateDesktopA (ANSI)
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
 - CreateDesktopA
 - winuser/CreateDesktopA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-1.dll
 - API-MS-Win-RTCore-NTUser-WindowStation-L1-1-0.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - CreateDesktop
 - CreateDesktopA
 - CreateDesktopW
req.apiset: ext-ms-win-ntuser-windowstation-l1-1-0 (introduced in Windows 8)
---

# CreateDesktopA function


## -description

Creates a new desktop, associates it with the current window station of the calling process, and assigns it to the calling thread. The calling process must have an associated window station, either assigned by the system at process creation time or set by 
the <a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a> function.

To specify the size of the heap for the desktop, use the <a href="/windows/desktop/api/winuser/nf-winuser-createdesktopexa">CreateDesktopEx</a> function.

## -parameters

### -param lpszDesktop [in]

The name of the desktop to be created. Desktop names are case-insensitive and may not contain backslash characters (\\).

### -param lpszDevice

Reserved; must be <b>NULL</b>.

### -param pDevmode

Reserved; must be <b>NULL</b>.

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
Enables processes running in other accounts on the desktop to set hooks in this process.

</td>
</tr>
</table>

### -param dwDesiredAccess [in]

The access to the desktop. For a list of values, see 
<a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>.

This parameter must include the <b>DESKTOP_CREATEWINDOW</b> access right, because internally 
<b>CreateDesktop</b> uses the handle to create a window.

### -param lpsa [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpsa</i> is NULL, the handle cannot be inherited.

The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new desktop. If this parameter is NULL, the desktop inherits its security descriptor from the parent window station.

## -returns

If the function succeeds, the return value is a handle to the newly created desktop. If the specified desktop already exists, the function succeeds and returns a handle to the existing desktop. When you are finished using the handle, call the 
<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a> function to close it.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>dwDesiredAccess</i> parameter specifies the <b>READ_CONTROL</b>, <b>WRITE_DAC</b>, or <b>WRITE_OWNER</b> standard access rights, you must also request the <b>DESKTOP_READOBJECTS</b> and <b>DESKTOP_WRITEOBJECTS</b> access rights.

The number of desktops that can be created is limited by the size of the system desktop heap, which is 48 MB. Desktop objects use the heap to store resources. You can increase the number of desktops that can be created by reducing the default heap reserved for each desktop in the interactive window station. This value is specified in the "SharedSection" substring of the following registry value: <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\SubSystems\Windows</b>. The default data for this registry value is as follows:

"%SystemRoot%\system32\csrss.exe ObjectDirectory=\Windows
SharedSection=1024,3072,512 Windows=On SubSystemType=Windows
ServerDll=basesrv,1 ServerDll=winsrv:UserServerDllInitialization,3
ServerDll=winsrv:ConServerDllInitialization,2 ProfileControl=Off
MaxRequestThreads=16"


The values for the "SharedSection" substring are described as follows:

<ul>
<li>The first "SharedSection" value is the size of the shared heap common to all desktops, in kilobytes.</li>
<li>The second "SharedSection" value is the size of the desktop heap needed for each desktop that is created in the interactive window station, WinSta0, in kilobytes.</li>
<li>The third "SharedSection" value is the size of the desktop heap needed for each desktop that is created in a noninteractive window station, in kilobytes.</li>
</ul>






> [!NOTE]
> The winuser.h header defines CreateDesktop as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopexa">CreateDesktopEx</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-switchdesktop">SwitchDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
