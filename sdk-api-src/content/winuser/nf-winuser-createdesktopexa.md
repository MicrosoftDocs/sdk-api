---
UID: NF:winuser.CreateDesktopExA
title: CreateDesktopExA function (winuser.h)
description: Creates a new desktop with the specified heap, associates it with the current window station of the calling process, and assigns it to the calling thread. (ANSI)
helpviewer_keywords: ["CreateDesktopExA", "DF_ALLOWOTHERACCOUNTHOOK", "winuser/CreateDesktopExA"]
old-location: winstation\createdesktopex.htm
tech.root: winstation
ms.assetid: 2fe8859d-1fe3-4f44-aa97-58e61779c4cc
ms.date: 12/05/2018
ms.keywords: CreateDesktopEx, CreateDesktopEx function [Windows Stations and Desktops], CreateDesktopExA, CreateDesktopExW, DF_ALLOWOTHERACCOUNTHOOK, base.createdesktopex, winstation.createdesktopex, winuser/CreateDesktopEx, winuser/CreateDesktopExA, winuser/CreateDesktopExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateDesktopExW (Unicode) and CreateDesktopExA (ANSI)
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
 - CreateDesktopExA
 - winuser/CreateDesktopExA
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
 - CreateDesktopEx
 - CreateDesktopExA
 - CreateDesktopExW
---

# CreateDesktopExA function


## -description

Creates a new desktop with the specified heap, associates it with the current window station of the calling process, and assigns it to the calling thread. The calling process must have an associated window station, either assigned by the system at process creation time or set by 
the <a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a> function.

## -parameters

### -param lpszDesktop [in]

The name of the desktop to be created. Desktop names are case-insensitive and may not contain backslash characters (\\).

### -param lpszDevice

This parameter is reserved and must be NULL.

### -param pDevmode

This parameter is reserved and must be NULL.

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

The requested access to the desktop. For a list of values, see 
<a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktop Security and Access Rights</a>. 




This parameter must include the DESKTOP_CREATEWINDOW access right, because internally 
<a href="/windows/desktop/api/winuser/nf-winuser-createdesktopa">CreateDesktop</a> uses the handle to create a window.

### -param lpsa [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpsa</i> is NULL, the handle cannot be inherited. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new desktop. If this parameter is NULL, the desktop inherits its security descriptor from the parent window station.

### -param ulHeapSize [in]

The size of the desktop heap, in kilobytes.

### -param pvoid

This parameter is reserved and must be NULL.

## -returns

If the function succeeds, the return value is a handle to the newly created desktop. If the specified desktop already exists, the function succeeds and returns a handle to the existing desktop. When you are finished using the handle, call the 
<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a> function to close it.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the <i>dwDesiredAccess</i> parameter specifies the READ_CONTROL, WRITE_DAC, or WRITE_OWNER standard access rights, you must also request the DESKTOP_READOBJECTS and DESKTOP_WRITEOBJECTS access rights.

The number of desktops that can be created is limited by the size of the system desktop heap. Desktop objects use the heap to store resources. You can increase the number of desktops that can be created by increasing the size of the desktop heap or by reducing the default heap reserved for each desktop in the interactive window station. This value is specified in the SharedSection substring of the following registry value: <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager\SubSystems\Windows</b>. The default data for this registry value is as follows:

%SystemRoot%\system32\csrss.exe ObjectDirectory=\Windows
SharedSection=1024,3072,512 Windows=On SubSystemType=Windows
ServerDll=basesrv,1 ServerDll=winsrv:UserServerDllInitialization,3
ServerDll=winsrv:ConServerDllInitialization,2 ProfileControl=Off
MaxRequestThreads=16


The values for the SharedSection substring are described as follows:

<ul>
<li>The first SharedSection value is the size of the shared heap common to all desktops, in kilobytes.</li>
<li>The second SharedSection value is the size of the desktop heap needed for each desktop that is created in the interactive window station, WinSta0, in kilobytes.</li>
<li>The third SharedSection value is the size of the desktop heap needed for each desktop that is created in a noninteractive window station, in kilobytes.</li>
</ul>


The default size of the desktop heap depends on factors such as hardware architecture. To retrieve the size of the desktop heap, call the <a href="/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa">GetUserObjectInformation</a> function with UOI_HEAPSIZE.





> [!NOTE]
> The winuser.h header defines CreateDesktopEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-closedesktop">CloseDesktop</a>



<a href="/windows/desktop/winstation/desktops">Desktops</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setprocesswindowstation">SetProcessWindowStation</a>



<a href="/windows/desktop/api/winuser/nf-winuser-switchdesktop">SwitchDesktop</a>



<a href="/windows/desktop/winstation/window-station-and-desktop-functions">Window Station and Desktop Functions</a>
