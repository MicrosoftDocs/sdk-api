---
UID: NF:winuser.OpenDesktopW
title: OpenDesktopW function
author: windows-sdk-content
description: Opens the specified desktop object.
old-location: winstation\opendesktop.htm
old-project: winstation
ms.assetid: 7f805f47-1737-4f4b-a74a-9c1423b65f2c
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: DF_ALLOWOTHERACCOUNTHOOK, OpenDesktop, OpenDesktop function [Windows Stations and Desktops], OpenDesktopA, OpenDesktopW, _win32_opendesktop, base.opendesktop, winstation.opendesktop, winuser/OpenDesktop, winuser/OpenDesktopA, winuser/OpenDesktopW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
<a href="https://msdn.microsoft.com/6512d128-3b0c-4ba7-8709-2fd225389a40">Desktop Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is a handle to the opened desktop. When you are finished using the handle, call the 
<a href="https://msdn.microsoft.com/861e57b2-061c-4598-ad38-6aef7b79ca54">CloseDesktop</a> function to close it.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The calling process must have an associated window station, either assigned by the system at process creation time or set by the 
<a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a> function.

If the <i>dwDesiredAccess</i> parameter specifies the <b>READ_CONTROL</b>, <b>WRITE_DAC</b>, or <b>WRITE_OWNER</b> standard access rights, you must also request the <b>DESKTOP_READOBJECTS</b> and <b>DESKTOP_WRITEOBJECTS</b> access rights.




## -see-also




<a href="https://msdn.microsoft.com/861e57b2-061c-4598-ad38-6aef7b79ca54">CloseDesktop</a>



<a href="https://msdn.microsoft.com/c6ed40c5-13a9-4697-a727-730adc6a912d">CreateDesktop</a>



<a href="https://msdn.microsoft.com/c56cd63b-c260-40d0-9a62-1dee1eb18679">Desktops</a>



<a href="https://msdn.microsoft.com/023d421e-bf32-4e08-b5b3-b7b2ca6c4e00">OpenInputDesktop</a>



<a href="https://msdn.microsoft.com/d64814a7-945c-4e73-a977-5f696d60610e">SetProcessWindowStation</a>



<a href="https://msdn.microsoft.com/619c591f-54b7-4b61-aa07-fc57e05ee37a">SetThreadDesktop</a>



<a href="https://msdn.microsoft.com/401be515-ada9-42be-b8e8-4e86f513bb8d">SwitchDesktop</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>
 

 

