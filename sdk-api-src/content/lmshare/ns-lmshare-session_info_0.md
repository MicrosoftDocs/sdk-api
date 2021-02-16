---
UID: NS:lmshare._SESSION_INFO_0
title: SESSION_INFO_0 (lmshare.h)
description: Contains the name of the computer that established the session.
helpviewer_keywords: ["*LPSESSION_INFO_0","*PSESSION_INFO_0","LPSESSION_INFO_0","LPSESSION_INFO_0 structure pointer [Files]","PSESSION_INFO_0","PSESSION_INFO_0 structure pointer [Files]","SESSION_INFO_0","SESSION_INFO_0 structure [Files]","_win32_session_info_0_str","fs.session_info_0_str","lmshare/LPSESSION_INFO_0","lmshare/PSESSION_INFO_0","lmshare/SESSION_INFO_0","netmgmt.session_info_0_str"]
old-location: fs\session_info_0_str.htm
tech.root: fs
ms.assetid: 6b39df47-f25c-41dd-ba15-6e6806c4ec89
ms.date: 12/05/2018
ms.keywords: '*LPSESSION_INFO_0, *PSESSION_INFO_0, LPSESSION_INFO_0, LPSESSION_INFO_0 structure pointer [Files], PSESSION_INFO_0, PSESSION_INFO_0 structure pointer [Files], SESSION_INFO_0, SESSION_INFO_0 structure [Files], _win32_session_info_0_str, fs.session_info_0_str, lmshare/LPSESSION_INFO_0, lmshare/PSESSION_INFO_0, lmshare/SESSION_INFO_0, netmgmt.session_info_0_str'
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
req.typenames: SESSION_INFO_0, *PSESSION_INFO_0, *LPSESSION_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SESSION_INFO_0
 - lmshare/_SESSION_INFO_0
 - PSESSION_INFO_0
 - lmshare/PSESSION_INFO_0
 - SESSION_INFO_0
 - lmshare/SESSION_INFO_0
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
 - SESSION_INFO_0
---

# SESSION_INFO_0 structure


## -description

Contains the name of the computer that established the session.

## -struct-fields

### -field sesi0_cname

Pointer to a Unicode string that contains the name of the computer that established the session. This string cannot contain a backslash (\\).

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo">NetSessionGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/session-functions">Session Functions</a>