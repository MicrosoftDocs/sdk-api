---
UID: NF:winuser.CreateDesktopExA
title: CreateDesktopExA function
author: windows-sdk-content
description: Creates a new desktop with the specified heap, associates it with the current window station of the calling process, and assigns it to the calling thread.
old-location: winstation\createdesktopex.htm
tech.root: winstation
ms.assetid: 2fe8859d-1fe3-4f44-aa97-58e61779c4cc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateDesktopEx, CreateDesktopEx function [Windows Stations and Desktops], CreateDesktopExA, CreateDesktopExW, DF_ALLOWOTHERACCOUNTHOOK, base.createdesktopex, winstation.createdesktopex, winuser/CreateDesktopEx, winuser/CreateDesktopExA, winuser/CreateDesktopExW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDesktopExA function


## -description


Creates a new desktop with the specified heap, associates it with the current window station of the calling process, and assigns it to the calling thread. The calling process must have an associated window station, either assigned by the system at process creation time or set by 
the <a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a> function.


## -parameters




### -param lpszDesktop [in]

The name of the desktop to be created. Desktop names are case-insensitive and may not contain backslash characters (\).


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
<a href="https://msdn.microsoft.com/6512d128-3b0c-4ba7-8709-2fd225389a40">Desktop Security and Access Rights</a>. 




This parameter must include the DESKTOP_CREATEWINDOW access right, because internally 
<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a> uses the handle to create a window.


### -param lpsa [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpsa</i> is NULL, the handle cannot be inherited. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new desktop. If this parameter is NULL, the desktop inherits its security descriptor from the parent window station.


### -param ulHeapSize [in]

The size of the desktop heap, in kilobytes. 


### -param pvoid

This parameter is reserved and must be NULL.


## -returns



If the function succeeds, the return value is a handle to the newly created desktop. If the specified desktop already exists, the function succeeds and returns a handle to the existing desktop. When you are finished using the handle, call the 
<a href="https://msdn.microsoft.com/861e57b2-061c-4598-ad38-6aef7b79ca54">CloseDesktop</a> function to close it.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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


The default size of the desktop heap depends on factors such as hardware architecture. To retrieve the size of the desktop heap, call the <a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a> function with UOI_HEAPSIZE.




## -see-also




<a href="https://msdn.microsoft.com/861e57b2-061c-4598-ad38-6aef7b79ca54">CloseDesktop</a>



<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/401be515-ada9-42be-b8e8-4e86f513bb8d">SwitchDesktop</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

