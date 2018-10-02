---
UID: NS:lmshare._SESSION_INFO_10
title: "_SESSION_INFO_10"
author: windows-sdk-content
description: Contains information about the session, including name of the computer; name of the user; and active and idle times for the session.
old-location: fs\session_info_10_str.htm
tech.root: NetShare
ms.assetid: a23a5647-f99d-4cb8-9d84-93653a3e7428
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPSESSION_INFO_10, *PSESSION_INFO_10, LPSESSION_INFO_10, LPSESSION_INFO_10 structure pointer [Files], PSESSION_INFO_10, PSESSION_INFO_10 structure pointer [Files], SESSION_INFO_10, SESSION_INFO_10 structure [Files], _SESSION_INFO_10, _win32_session_info_10_str, fs.session_info_10_str, lmshare/LPSESSION_INFO_10, lmshare/PSESSION_INFO_10, lmshare/SESSION_INFO_10, netmgmt.session_info_10_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - Lmshare.h
api_name:
 - SESSION_INFO_10
product: Windows
targetos: Windows
req.typenames: SESSION_INFO_10, *PSESSION_INFO_10, *LPSESSION_INFO_10
req.redist: 
---

# _SESSION_INFO_10 structure


## -description


Contains information about the session, including name of the computer; name of the user; and active and idle times for the session.


## -struct-fields




### -field sesi10_cname

Pointer to a Unicode string specifying the name of the computer that established the session. This string cannot contain a backslash (\).


### -field sesi10_username

Pointer to a Unicode string specifying the name of the user who established the session.


### -field sesi10_time

Specifies the number of seconds the session has been active.


### -field sesi10_idle_time

Specifies the number of seconds the session has been idle.


## -see-also




<a href="https://msdn.microsoft.com/5923a8cc-bf7a-4ffa-b089-fd7f26ee42d2">NetSessionEnum</a>



<a href="https://msdn.microsoft.com/d44fb8d8-2b64-4268-8603-7784e2c5f2d5">NetSessionGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/931455e3-1301-4a68-93c3-2674b3d4c491">Session Functions</a>
 

 

