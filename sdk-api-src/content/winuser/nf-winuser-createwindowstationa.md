---
UID: NF:winuser.CreateWindowStationA
title: CreateWindowStationA function
author: windows-sdk-content
description: Creates a window station object, associates it with the calling process, and assigns it to the current session.
old-location: winstation\createwindowstation.htm
tech.root: winstation
ms.assetid: c1aee546-decd-46c9-8d02-d6792f5a6a0d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateWindowStation, CreateWindowStation function [Windows Stations and Desktops], CreateWindowStationA, CreateWindowStationW, _win32_createwindowstation, base.createwindowstation, winstation.createwindowstation, winuser/CreateWindowStation, winuser/CreateWindowStationA, winuser/CreateWindowStationW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateWindowStationW (Unicode) and CreateWindowStationA (ANSI)
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
 - API-MS-Win-RTCore-NTUser-WindowStation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-0.dll
 - Ext-MS-Win-NTUser-Windowstation-L1-1-1.dll
 - Ext-MS-Win-NTUser-WindowStation-L1-1-2.dll
api_name:
 - CreateWindowStation
 - CreateWindowStationA
 - CreateWindowStationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateWindowStationA function


## -description


Creates a window station object, associates it with the calling process, and assigns it to the current session.


## -parameters




### -param lpwinsta [in, optional]

The name of the window station to be created. Window station names are case-insensitive and cannot contain backslash characters (\). Only members of the Administrators group are allowed to specify a name. If <i>lpwinsta</i> is <b>NULL</b> or an empty string, the system forms a window station name using the logon session identifier for the calling process. To get this name, call the 
<a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a> function.


### -param dwFlags

If this parameter is <b>CWF_CREATE_ONLY</b> and the window station already exists, the call fails. If this flag is not specified and the window station already exists, the function succeeds and returns a new handle to the existing window station.

<b>Windows XP/2000:  </b>This parameter is reserved and must be zero.


### -param dwDesiredAccess [in]

The type of access the returned handle has to the window station. In addition, you can specify any of the standard access rights, such as <b>READ_CONTROL</b> or <b>WRITE_DAC</b>, and a combination of the window station-specific access rights. For more information, see <a href="https://msdn.microsoft.com/b132da61-26b7-4457-9433-4894ca0e640a">Window Station Security and Access Rights</a>.


### -param lpsa [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpsa</i> is <b>NULL</b>, the handle cannot be inherited.

The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new window station. If <i>lpsa</i> is <b>NULL</b>, the window station (and any desktops created within the window) gets a security descriptor that grants <b>GENERIC_ALL</b> access to all users.


## -returns



If the function succeeds, the return value is a handle to the newly created window station. If the specified window station already exists, the function succeeds and returns a handle to the existing window station.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After you are done with the handle, you must call 
<a href="https://msdn.microsoft.com/417cb01b-c206-4b5b-9516-94e5d90717f4">CloseWindowStation</a> to free the handle.




## -see-also




<a href="https://msdn.microsoft.com/417cb01b-c206-4b5b-9516-94e5d90717f4">CloseWindowStation</a>



<a href="https://msdn.microsoft.com/64f7361d-1a94-4d5b-86f1-a2a21737668a">GetUserObjectInformation</a>



<a href="https://msdn.microsoft.com/78ee7100-1bad-4c2d-b923-c5e67191bd41">OpenWindowStation</a>



<a href="https://msdn.microsoft.com/6214c28f-1035-446c-8c79-5d1dd638af2a">Window Station and Desktop Functions</a>



<a href="https://msdn.microsoft.com/617661e2-3b0d-42a9-9769-2ba0957c31a8">Window Stations</a>
 

 

