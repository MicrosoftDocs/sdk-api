---
UID: NS:lmshare._SESSION_INFO_502
title: SESSION_INFO_502 (lmshare.h)
description: Contains information about the session, including name of the computer; name of the user; open files, pipes, and devices on the computer; and the name of the transport the client is using.
helpviewer_keywords: ["*LPSESSION_INFO_502","*PSESSION_INFO_502","DOS LM 1.0","DOS LM 2.0","LPSESSION_INFO_502","LPSESSION_INFO_502 structure pointer [Files]","OS/2 LM 1.0","OS/2 LM 2.0","PSESSION_INFO_502","PSESSION_INFO_502 structure pointer [Files]","SESSION_INFO_502","SESSION_INFO_502 structure [Files]","SESS_GUEST","SESS_NOENCRYPTION","_win32_session_info_502_str","fs.session_info_502_str","lmshare/LPSESSION_INFO_502","lmshare/PSESSION_INFO_502","lmshare/SESSION_INFO_502","netmgmt.session_info_502_str"]
old-location: fs\session_info_502_str.htm
tech.root: fs
ms.assetid: a86a00ae-f60a-4b12-a9ac-4b96f9abd6a2
ms.date: 12/05/2018
ms.keywords: '*LPSESSION_INFO_502, *PSESSION_INFO_502, DOS LM 1.0, DOS LM 2.0, LPSESSION_INFO_502, LPSESSION_INFO_502 structure pointer [Files], OS/2 LM 1.0, OS/2 LM 2.0, PSESSION_INFO_502, PSESSION_INFO_502 structure pointer [Files], SESSION_INFO_502, SESSION_INFO_502 structure [Files], SESS_GUEST, SESS_NOENCRYPTION, _win32_session_info_502_str, fs.session_info_502_str, lmshare/LPSESSION_INFO_502, lmshare/PSESSION_INFO_502, lmshare/SESSION_INFO_502, netmgmt.session_info_502_str'
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
req.typenames: SESSION_INFO_502, *PSESSION_INFO_502, *LPSESSION_INFO_502
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SESSION_INFO_502
 - lmshare/_SESSION_INFO_502
 - PSESSION_INFO_502
 - lmshare/PSESSION_INFO_502
 - SESSION_INFO_502
 - lmshare/SESSION_INFO_502
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
 - SESSION_INFO_502
---

# SESSION_INFO_502 structure


## -description

Contains information about the session, including name of the computer; name of the user; open files, pipes, and devices on the computer; and the name of the transport the client is using.

## -struct-fields

### -field sesi502_cname

Pointer to a Unicode string specifying the name of the computer that established the session. This string cannot contain a backslash (\\).

### -field sesi502_username

Pointer to a Unicode string specifying the name of the user who established the session.

### -field sesi502_num_opens

Specifies the number of files, devices, and pipes opened during the session.

### -field sesi502_time

Specifies the number of seconds the session has been active.

### -field sesi502_idle_time

Specifies the number of seconds the session has been idle.

### -field sesi502_user_flags

Specifies a value that describes how the user established the session. This member can be one of the following values. 



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
The user specified by the <b>sesi502_username</b> member established the session using a guest account.

</td>
</tr>
<tr>
<td width="40%"><a id="SESS_NOENCRYPTION"></a><a id="sess_noencryption"></a><dl>
<dt><b>SESS_NOENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
The user specified by the <b>sesi502_username</b> member established the session without using password encryption.

</td>
</tr>
</table>

### -field sesi502_cltype_name

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
LAN Manager for MS-DOS 1.0 clients.

</td>
</tr>
<tr>
<td width="40%"><a id="DOS_LM_2.0"></a><a id="dos_lm_2.0"></a><dl>
<dt><b>DOS LM 2.0</b></dt>
</dl>
</td>
<td width="60%">
LAN Manager for MS-DOS 2.0 clients.

</td>
</tr>
<tr>
<td width="40%"><a id="OS_2_LM_1.0"></a><a id="os_2_lm_1.0"></a><dl>
<dt><b>OS/2 LM 1.0</b></dt>
</dl>
</td>
<td width="60%">
LAN Manager for MS-OS/2 1.0 clients.

</td>
</tr>
<tr>
<td width="40%"><a id="OS_2_LM_2.0"></a><a id="os_2_lm_2.0"></a><dl>
<dt><b>OS/2 LM 2.0</b></dt>
</dl>
</td>
<td width="60%">
LAN Manager for MS-OS/2 2.0 clients.

</td>
</tr>
</table>
 

Sessions from LAN Manager servers running UNIX also will appear as LAN Manager 2.0.

### -field sesi502_transport

Specifies the name of the transport that the client is using to communicate with the server.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum">NetSessionEnum</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/session-functions">Session Functions</a>