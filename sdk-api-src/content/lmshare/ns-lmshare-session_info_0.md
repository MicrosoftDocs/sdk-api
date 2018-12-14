---
UID: NS:lmshare._SESSION_INFO_0
title: SESSION_INFO_0
author: windows-sdk-content
description: Contains the name of the computer that established the session.
old-location: fs\session_info_0_str.htm
tech.root: NetShare
ms.assetid: 6b39df47-f25c-41dd-ba15-6e6806c4ec89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSESSION_INFO_0, *PSESSION_INFO_0, LPSESSION_INFO_0, LPSESSION_INFO_0 structure pointer [Files], PSESSION_INFO_0, PSESSION_INFO_0 structure pointer [Files], SESSION_INFO_0, SESSION_INFO_0 structure [Files], _win32_session_info_0_str, fs.session_info_0_str, lmshare/LPSESSION_INFO_0, lmshare/PSESSION_INFO_0, lmshare/SESSION_INFO_0, netmgmt.session_info_0_str"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SESSION_INFO_0
product: Windows
targetos: Windows
req.typenames: SESSION_INFO_0, *PSESSION_INFO_0, *LPSESSION_INFO_0
req.redist: 
---

# SESSION_INFO_0 structure


## -description


Contains the name of the computer that established the session.


## -struct-fields




### -field sesi0_cname

Pointer to a Unicode string that contains the name of the computer that established the session. This string cannot contain a backslash (\).


## -see-also




<a href="https://msdn.microsoft.com/5923a8cc-bf7a-4ffa-b089-fd7f26ee42d2">NetSessionEnum</a>



<a href="https://msdn.microsoft.com/d44fb8d8-2b64-4268-8603-7784e2c5f2d5">NetSessionGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/931455e3-1301-4a68-93c3-2674b3d4c491">Session Functions</a>
 

 

