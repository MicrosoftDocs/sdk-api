---
UID: NF:wtsapi32.WTSEnumerateSessionsExA
title: WTSEnumerateSessionsExA function
author: windows-sdk-content
description: Retrieves a list of sessions on a specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.
old-location: termserv\wtsenumeratesessionsex.htm
old-project: TermServ
ms.assetid: b903cf07-d3bd-4b65-9e57-88d9e1f74e0b
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: WTSEnumerateSessionsEx, WTSEnumerateSessionsEx function [Remote Desktop Services], WTSEnumerateSessionsExA, WTSEnumerateSessionsExW, termserv.wtsenumeratesessionsex, wtsapi32/WTSEnumerateSessionsEx, wtsapi32/WTSEnumerateSessionsExA, wtsapi32/WTSEnumerateSessionsExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateSessionsExW (Unicode) and WTSEnumerateSessionsExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WTS_VIRTUAL_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wtsapi32.dll
 - Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
 - WTSEnumerateSessionsEx
 - WTSEnumerateSessionsExA
 - WTSEnumerateSessionsExW
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSEnumerateSessionsExA function


## -description


Retrieves a list of sessions on a specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.


## -parameters




### -param hServer [in]

A handle to the target server. Specify a handle returned by the 
<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> or <a href="https://msdn.microsoft.com/8122de66-c096-4bd8-95ff-ed64b88afcae">WTSOpenServerEx</a> function. To enumerate sessions on  the RD Session Host server on which the application is running, specify <b>WTS_CURRENT_SERVER_HANDLE</b>.


### -param pLevel [in, out]

This parameter is reserved. Always set this parameter to one. On output, <b>WTSEnumerateSessionsEx</b> does not change the value of this parameter.


### -param Filter [in]

This parameter is reserved. Always set this parameter to zero.


### -param ppSessionInfo [out]

A pointer to a <b>PWTS_SESSION_INFO_1</b> variable that receives a pointer to an array of 
<a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a> structures. Each structure in the array contains information about a session on the specified RD Session Host server. If you obtained a handle to an RD Virtualization Host server by calling the <a href="https://msdn.microsoft.com/8122de66-c096-4bd8-95ff-ed64b88afcae">WTSOpenServerEx</a> function, the array contains information about sessions on virtual machines on the server. When you have finished using the array, free it by calling the <a href="https://msdn.microsoft.com/d84a4fe3-a829-4cf3-b217-157391d0c495">WTSFreeMemoryEx</a> function. You should also set the pointer to <b>NULL</b>.


### -param pCount [out]

A pointer to a <b>DWORD</b> variable that receives the number of 
<a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a> structures returned in the <i>ppSessionInfo</i> buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



To obtain information about sessions running on virtual machines on an RD Virtualization Host server, you must obtain the handle by calling the <a href="https://msdn.microsoft.com/8122de66-c096-4bd8-95ff-ed64b88afcae">WTSOpenServerEx</a> function. To free the returned buffer, call the 
<a href="https://msdn.microsoft.com/d84a4fe3-a829-4cf3-b217-157391d0c495">WTSFreeMemoryEx</a> function and set the <i>WTSClassType</i> parameter to <b>WTSTypeSessionInfoLevel1</b>.

To enumerate a session, you need to have the Query Information permission for that session. For more information, see 
<a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.

To enumerate sessions running on a virtual machine hosted on an RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.




## -see-also




<a href="https://msdn.microsoft.com/d84a4fe3-a829-4cf3-b217-157391d0c495">WTSFreeMemoryEx</a>



<a href="https://msdn.microsoft.com/8122de66-c096-4bd8-95ff-ed64b88afcae">WTSOpenServerEx</a>



<a href="https://msdn.microsoft.com/29d76033-d61d-4bc5-b47a-f7dea9543f23">WTS_SESSION_INFO_1</a>
 

 

