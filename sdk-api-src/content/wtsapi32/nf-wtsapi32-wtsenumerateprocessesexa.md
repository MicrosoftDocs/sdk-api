---
UID: NF:wtsapi32.WTSEnumerateProcessesExA
title: WTSEnumerateProcessesExA function (wtsapi32.h)
description: Retrieves information about the active processes on the specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.
helpviewer_keywords: ["WTSEnumerateProcessesEx","WTSEnumerateProcessesEx function [Remote Desktop Services]","WTSEnumerateProcessesExA","WTSEnumerateProcessesExW","termserv.wtsenumerateprocessesex","wtsapi32/WTSEnumerateProcessesEx","wtsapi32/WTSEnumerateProcessesExA","wtsapi32/WTSEnumerateProcessesExW"]
old-location: termserv\wtsenumerateprocessesex.htm
tech.root: TermServ
ms.assetid: bc8a2550-cf89-4203-b96b-c750c0dff255
ms.date: 12/05/2018
ms.keywords: WTSEnumerateProcessesEx, WTSEnumerateProcessesEx function [Remote Desktop Services], WTSEnumerateProcessesExA, WTSEnumerateProcessesExW, termserv.wtsenumerateprocessesex, wtsapi32/WTSEnumerateProcessesEx, wtsapi32/WTSEnumerateProcessesExA, wtsapi32/WTSEnumerateProcessesExW
f1_keywords:
- wtsapi32/WTSEnumerateProcessesEx
dev_langs:
- c++
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSEnumerateProcessesExW (Unicode) and WTSEnumerateProcessesExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wtsapi32.lib
req.dll: Wtsapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wtsapi32.dll
- Ext-MS-Win-Session-WtsApi32-l1-1-0.dll
api_name:
- WTSEnumerateProcessesEx
- WTSEnumerateProcessesExA
- WTSEnumerateProcessesExW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WTSEnumerateProcessesExA function


## -description


Retrieves information about the active 
    processes on the specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Specify a handle opened by the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a> function, or specify 
      <b>WTS_CURRENT_SERVER_HANDLE</b> to indicate the server on which your application is 
      running.


### -param pLevel [in, out]

A pointer to a <b>DWORD</b> variable that, on input, specifies the type of information  to return. To return an array of <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_infoa">WTS_PROCESS_INFO</a> structures, specify zero. To return an array of <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa">WTS_PROCESS_INFO_EX</a> structures, specify one.

If you do not specify a valid value for this parameter, on output, <b>WTSEnumerateProcessesEx</b> sets this parameter to one and returns an error. Otherwise, on output, <b>WTSEnumerateProcessesEx</b> does not change the value of this parameter.


### -param SessionId [in]

The session  for which to enumerate processes. To enumerate processes for all sessions on the server,  specify <b>WTS_ANY_SESSION</b>.


### -param ppProcessInfo [out]

A pointer to a variable that receives a pointer to an array of 
      <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_infoa">WTS_PROCESS_INFO</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa">WTS_PROCESS_INFO_EX</a> structures. The type of structure is determined by the value passed to the <i>pLevel</i> parameter. Each structure 
      in the array contains information about an active process. When you have finished using the array, free it by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsfreememoryexa">WTSFreeMemoryEx</a> function. You should also set the pointer to <b>NULL</b>.


### -param pCount [out]

A pointer to a variable that receives the number of  
      structures returned in the buffer referenced by the <i>ppProcessInfo</i> parameter.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



The caller must be a member of the Administrators group to enumerate processes that are running under another user session.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsopenservera">WTSOpenServer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_infoa">WTS_PROCESS_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_process_info_exa">WTS_PROCESS_INFO_EX</a>
 

 

