---
UID: NS:wtsapi32._WTS_PROCESS_INFOA
title: WTS_PROCESS_INFOA (wtsapi32.h)
author: windows-sdk-content
description: Contains information about a process running on a Remote Desktop Session Host (RD Session Host) server.
old-location: termserv\wts_process_info_str.htm
tech.root: TermServ
ms.assetid: 5df01ad8-71fd-4831-8eba-1d6cabd61348
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWTS_PROCESS_INFOA, PWTS_PROCESS_INFO, PWTS_PROCESS_INFO structure pointer [Remote Desktop Services], WTS_PROCESS_INFO, WTS_PROCESS_INFO structure [Remote Desktop Services], WTS_PROCESS_INFOA, WTS_PROCESS_INFOW, _win32_wts_process_info_str, termserv.wts_process_info_str, wtsapi32/PWTS_PROCESS_INFO, wtsapi32/WTS_PROCESS_INFO, wtsapi32/WTS_PROCESS_INFOA, wtsapi32/WTS_PROCESS_INFOW"
ms.topic: struct
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTS_PROCESS_INFOW (Unicode) and WTS_PROCESS_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTS_PROCESS_INFO
 - WTS_PROCESS_INFOA
 - WTS_PROCESS_INFOW
product: Windows
targetos: Windows
req.typenames: WTS_PROCESS_INFOA, *PWTS_PROCESS_INFOA
req.redist: 
ms.custom: 19H1
---

# WTS_PROCESS_INFOA structure


## -description


Contains information about a process running on a Remote Desktop Session Host (RD Session Host) server.


## -struct-fields




### -field SessionId

Remote Desktop Services session identifier for the session associated with the process.


### -field ProcessId

Process identifier that uniquely identifies the process on the RD Session Host server.


### -field pProcessName

Pointer to a null-terminated string containing the name of the executable file associated with the process.


### -field pUserSid

Pointer to the user 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-identifiers">Security Identifiers</a> in the process's primary access token. For more information about SIDs and access tokens, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa">WTSEnumerateProcesses</a>
 

 

