---
UID: NS:lmshare._SESSION_INFO_10
title: SESSION_INFO_10 (lmshare.h)
description: Contains information about the session, including name of the computer; name of the user; and active and idle times for the session.
helpviewer_keywords: ["*LPSESSION_INFO_10","*PSESSION_INFO_10","LPSESSION_INFO_10","LPSESSION_INFO_10 structure pointer [Files]","PSESSION_INFO_10","PSESSION_INFO_10 structure pointer [Files]","SESSION_INFO_10","SESSION_INFO_10 structure [Files]","_win32_session_info_10_str","fs.session_info_10_str","lmshare/LPSESSION_INFO_10","lmshare/PSESSION_INFO_10","lmshare/SESSION_INFO_10","netmgmt.session_info_10_str"]
old-location: fs\session_info_10_str.htm
tech.root: fs
ms.assetid: a23a5647-f99d-4cb8-9d84-93653a3e7428
ms.date: 12/05/2018
ms.keywords: '*LPSESSION_INFO_10, *PSESSION_INFO_10, LPSESSION_INFO_10, LPSESSION_INFO_10 structure pointer [Files], PSESSION_INFO_10, PSESSION_INFO_10 structure pointer [Files], SESSION_INFO_10, SESSION_INFO_10 structure [Files], _win32_session_info_10_str, fs.session_info_10_str, lmshare/LPSESSION_INFO_10, lmshare/PSESSION_INFO_10, lmshare/SESSION_INFO_10, netmgmt.session_info_10_str'
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
targetos: Windows
req.typenames: SESSION_INFO_10, *PSESSION_INFO_10, *LPSESSION_INFO_10
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SESSION_INFO_10
 - lmshare/_SESSION_INFO_10
 - PSESSION_INFO_10
 - lmshare/PSESSION_INFO_10
 - SESSION_INFO_10
 - lmshare/SESSION_INFO_10
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmshare.h
api_name:
 - SESSION_INFO_10
---

# SESSION_INFO_10 structure


## -description

Contains information about the session, including name of the computer; name of the user; and active and idle times for the session.

## -struct-fields

### -field sesi10_cname

Pointer to a Unicode string specifying the name of the computer that established the session. This string cannot contain a backslash (\\).

### -field sesi10_username

Pointer to a Unicode string specifying the name of the user who established the session.

### -field sesi10_time

Specifies the number of seconds the session has been active.

### -field sesi10_idle_time

Specifies the number of seconds the session has been idle.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo">NetSessionGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/session-functions">Session Functions</a>