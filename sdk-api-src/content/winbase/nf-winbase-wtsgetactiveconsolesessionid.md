---
UID: NF:winbase.WTSGetActiveConsoleSessionId
title: WTSGetActiveConsoleSessionId function
author: windows-driver-content
description: Retrieves the session identifier of the console session.
old-location: termserv\wtsgetactiveconsolesessionid.htm
old-project: TermServ
ms.assetid: 9aa43cfa-9518-428b-95a1-004fa23df90b
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: WTSGetActiveConsoleSessionId, WTSGetActiveConsoleSessionId function [Remote Desktop Services], _win32_wtsgetactiveconsolesessionid, termserv.wtsgetactiveconsolesessionid, winbase/WTSGetActiveConsoleSessionId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	api-ms-win-core-kernel32-legacy-l1-1-0.dll
-	kernel32legacy.dll
-	api-ms-win-core-kernel32-legacy-l1-1-1.dll
-	api-ms-win-core-kernel32-legacy-l1-1-2.dll
-	api-ms-win-downlevel-kernel32-l2-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	WTSGetActiveConsoleSessionId
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WTSGetActiveConsoleSessionId function


## -description


Retrieves the session identifier of the console session. The console session is the session that is currently attached to the physical console. Note that it is not necessary that Remote Desktop Services be running for this 
    function to succeed.


## -parameters






## -returns



The session identifier of the session that is attached to the physical console. If there is no session attached to the 
       physical console, (for example, if the physical console session is in the process of being attached or detached), this function 
       returns 0xFFFFFFFF.




## -remarks



The session identifier returned by this function is the identifier of the current physical console session. To monitor 
    the state of the current physical console session, use the 
    <a href="https://msdn.microsoft.com/5067bb03-d8d5-41ce-b187-04d7dd22a028">WTSRegisterSessionNotification</a> 
    function.




## -see-also




<a href="https://msdn.microsoft.com/99a3f047-705c-40bc-8cc2-055257a4f2b3">ProcessIdToSessionId</a>



<a href="https://msdn.microsoft.com/758a130c-b75a-40fd-8530-3766aa86c5ba">WM_WTSSESSION_CHANGE</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>



<a href="https://msdn.microsoft.com/5067bb03-d8d5-41ce-b187-04d7dd22a028">WTSRegisterSessionNotification</a>
 

 

