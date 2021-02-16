---
UID: NS:lmshare._SESSION_INFO_2
title: SESSION_INFO_2 (lmshare.h)
description: Contains information about the session, including name of the computer; name of the user; open files, pipes, and devices on the computer; and the type of client that established the session.
helpviewer_keywords: ["*LPSESSION_INFO_2","*PSESSION_INFO_2","DOS LM 1.0","DOS LM 2.0","LPSESSION_INFO_2","LPSESSION_INFO_2 structure pointer [Files]","OS/2 LM 1.0","OS/2 LM 2.0","PSESSION_INFO_2","PSESSION_INFO_2 structure pointer [Files]","SESSION_INFO_2","SESSION_INFO_2 structure [Files]","SESS_GUEST","SESS_NOENCRYPTION","_win32_session_info_2_str","fs.session_info_2_str","lmshare/LPSESSION_INFO_2","lmshare/PSESSION_INFO_2","lmshare/SESSION_INFO_2","netmgmt.session_info_2_str"]
old-location: fs\session_info_2_str.htm
tech.root: fs
ms.assetid: c3429eba-4277-4dc7-9255-cd2ff18dc583
ms.date: 12/05/2018
ms.keywords: '*LPSESSION_INFO_2, *PSESSION_INFO_2, DOS LM 1.0, DOS LM 2.0, LPSESSION_INFO_2, LPSESSION_INFO_2 structure pointer [Files], OS/2 LM 1.0, OS/2 LM 2.0, PSESSION_INFO_2, PSESSION_INFO_2 structure pointer [Files], SESSION_INFO_2, SESSION_INFO_2 structure [Files], SESS_GUEST, SESS_NOENCRYPTION, _win32_session_info_2_str, fs.session_info_2_str, lmshare/LPSESSION_INFO_2, lmshare/PSESSION_INFO_2, lmshare/SESSION_INFO_2, netmgmt.session_info_2_str'
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
req.typenames: SESSION_INFO_2, *PSESSION_INFO_2, *LPSESSION_INFO_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SESSION_INFO_2
 - lmshare/_SESSION_INFO_2
 - PSESSION_INFO_2
 - lmshare/PSESSION_INFO_2
 - SESSION_INFO_2
 - lmshare/SESSION_INFO_2
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
 - SESSION_INFO_2
---

# SESSION_INFO_2 structure


## -description

Contains information about the session, including name of the computer; name of the user; open files, pipes, and devices on the computer; and the type of client that established the session.

## -struct-fields

### -field sesi2_cname

Pointer to a Unicode string specifying the name of the computer that established the session. This string cannot contain a backslash (\\).

### -field sesi2_username

Pointer to a Unicode string specifying the name of the user who established the session.

### -field sesi2_num_opens

Specifies a DWORD value that contains the number of files, devices, and pipes opened during the session.

### -field sesi2_time

Specifies a DWORD value that contains the number of seconds the session has been active.

### -field sesi2_idle_time

Specifies a DWORD value that contains the number of seconds the session has been idle.

### -field sesi2_user_flags

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
The user specified by the <b>sesi2_username</b> member established the session using a guest account.

</td>
</tr>
<tr>
<td width="40%"><a id="SESS_NOENCRYPTION"></a><a id="sess_noencryption"></a><dl>
<dt><b>SESS_NOENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
The user specified by the <b>sesi2_username</b> member established the session without using password encryption.

</td>
</tr>
</table>

### -field sesi2_cltype_name

Pointer to a Unicode string that specifies the type of client that established the session. Following are the defined types for LAN Manager servers. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DOS_LM_1.0"></a><a id="dos_lm_1.0"></a><dl>
<dt><b>DOS LM 1.0</b></dt>
</dl>
</td>
<td width="60%">
LAN Manager for MS-DOS 1.0 clients

</td>
</tr>
<tr>
<td width="40%"><a id="DOS_LM_2.0"></a><a id="dos_lm_2.0"></a><dl>
<dt><b>DOS LM 2.0</b></dt>
</dl>
</td>
<td width="60%">
LAN Manager for MS-DOS 2.0 clients

</td>
</tr>
<tr>
<td width="40%"><a id="OS_2_LM_1.0"></a><a id="os_2_lm_1.0"></a><dl>
<dt><b>OS/2 LM 1.0</b></dt>
</dl>
</td>
<td width="60%">
LAN Manager for MS-OS/2 1.0 clients

</td>
</tr>
<tr>
<td width="40%"><a id="OS_2_LM_2.0"></a><a id="os_2_lm_2.0"></a><dl>
<dt><b>OS/2 LM 2.0</b></dt>
</dl>
</td>
<td width="60%">
LAN Manager for MS-OS/2 2.0 clients

</td>
</tr>
</table>
 

Sessions from LAN Manager servers running UNIX also will appear as LAN Manager 2.0.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo">NetSessionGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/session-functions">Session Functions</a>