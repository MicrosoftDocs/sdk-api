---
UID: NF:wtsapi32.WTSLogoffSession
title: WTSLogoffSession function
author: windows-sdk-content
description: Logs off a specified Remote Desktop Services session.
old-location: termserv\wtslogoffsession.htm
old-project: TermServ
ms.assetid: dba7b6fb-f906-40d1-baae-6ee7b8cfe86d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: WTSLogoffSession, WTSLogoffSession function [Remote Desktop Services], _win32_wtslogoffsession, termserv.wtslogoffsession, wtsapi32/WTSLogoffSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - WTSLogoffSession
product: Windows
targetos: Windows
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WTSLogoffSession function


## -description


Logs off a specified Remote Desktop Services session.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> or <a href="https://msdn.microsoft.com/8122de66-c096-4bd8-95ff-ed64b88afcae">WTSOpenServerEx</a> function, or specify <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the RD Session Host server on which your application is running.


### -param SessionId [in]

A Remote Desktop Services session identifier. To indicate the current session, specify <b>WTS_CURRENT_SESSION</b>. You can use the 
<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a> function to retrieve the identifiers of all sessions on a specified RD Session Host server.

To be able to log off another user's session, you need to have the Reset permission. For more information, see 
<a href="https://msdn.microsoft.com/448a7f9b-bf12-48eb-a3e7-4512ec288d95">Remote Desktop Services Permissions</a>. To modify permissions on a session, use the Remote Desktop Services Configuration administrative tool.

To log off sessions running on a virtual machine hosted on a RD Virtualization Host server, you must be a member of the Administrators group on the RD Virtualization Host server.


### -param bWait [in]

Indicates whether the operation is synchronous.

If <i>bWait</i> is <b>TRUE</b>, the function returns when the session is logged off.

If <i>bWait</i> is <b>FALSE</b>, the function returns immediately. To verify that the session has been logged off, specify the session identifier in a call to the 
<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a> function. 
<b>WTSQuerySessionInformation</b> returns zero if the session is logged off.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/6f9dd7d4-48dc-411c-85f1-cd1239d1e106">WTSEnumerateSessions</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>
 

 

