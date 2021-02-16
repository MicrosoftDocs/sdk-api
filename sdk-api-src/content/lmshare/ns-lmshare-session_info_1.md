---
UID: NS:lmshare._SESSION_INFO_1
title: SESSION_INFO_1 (lmshare.h)
description: Contains information about the session, including name of the computer; name of the user; and open files, pipes, and devices on the computer.
helpviewer_keywords: ["*LPSESSION_INFO_1","*PSESSION_INFO_1","LPSESSION_INFO_1","LPSESSION_INFO_1 structure pointer [Files]","PSESSION_INFO_1","PSESSION_INFO_1 structure pointer [Files]","SESSION_INFO_1","SESSION_INFO_1 structure [Files]","SESS_GUEST","SESS_NOENCRYPTION","_win32_session_info_1_str","fs.session_info_1_str","lmshare/LPSESSION_INFO_1","lmshare/PSESSION_INFO_1","lmshare/SESSION_INFO_1","netmgmt.session_info_1_str"]
old-location: fs\session_info_1_str.htm
tech.root: fs
ms.assetid: bc1c985e-b8af-4134-9ae4-511d82e3909b
ms.date: 12/05/2018
ms.keywords: '*LPSESSION_INFO_1, *PSESSION_INFO_1, LPSESSION_INFO_1, LPSESSION_INFO_1 structure pointer [Files], PSESSION_INFO_1, PSESSION_INFO_1 structure pointer [Files], SESSION_INFO_1, SESSION_INFO_1 structure [Files], SESS_GUEST, SESS_NOENCRYPTION, _win32_session_info_1_str, fs.session_info_1_str, lmshare/LPSESSION_INFO_1, lmshare/PSESSION_INFO_1, lmshare/SESSION_INFO_1, netmgmt.session_info_1_str'
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
req.typenames: SESSION_INFO_1, *PSESSION_INFO_1, *LPSESSION_INFO_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SESSION_INFO_1
 - lmshare/_SESSION_INFO_1
 - PSESSION_INFO_1
 - lmshare/PSESSION_INFO_1
 - SESSION_INFO_1
 - lmshare/SESSION_INFO_1
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
 - SESSION_INFO_1
---

# SESSION_INFO_1 structure


## -description

Contains information about the session, including name of the computer; name of the user; and open files, pipes, and devices on the computer.

## -struct-fields

### -field sesi1_cname

Pointer to a Unicode string specifying the name of the computer that established the session. This string cannot contain a backslash (\\).

### -field sesi1_username

Pointer to a Unicode string specifying the name of the user who established the session.

### -field sesi1_num_opens

Specifies a DWORD value that contains the number of files, devices, and pipes opened during the session.

### -field sesi1_time

Specifies a DWORD value that contains the number of seconds the session has been active.

### -field sesi1_idle_time

Specifies a DWORD value that contains the number of seconds the session has been idle.

### -field sesi1_user_flags

Specifies a DWORD value that describes how the user established the session. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SESS_GUEST"></a><a id="sess_guest"></a><dl>
<dt><b>SESS_GUEST</b></dt>
</dl>
</td>
<td width="60%">
The user specified by the <b>sesi1_username</b> member established the session using a guest account.

</td>
</tr>
<tr>
<td width="40%"><a id="SESS_NOENCRYPTION"></a><a id="sess_noencryption"></a><dl>
<dt><b>SESS_NOENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
The user specified by the <b>sesi1_username</b> member established the session without using password encryption.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo">NetSessionGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/session-functions">Session Functions</a>