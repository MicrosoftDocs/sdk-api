---
UID: NS:lmuse._USE_INFO_1
title: USE_INFO_1 (lmuse.h)
description: Contains information about the connection between a local device and a shared resource.
helpviewer_keywords: ["*LPUSE_INFO_1","*PUSE_INFO_1","LPUSE_INFO_1","LPUSE_INFO_1 structure pointer [Network Management]","PUSE_INFO_1","PUSE_INFO_1 structure pointer [Network Management]","USE_CONN","USE_DISCONN","USE_DISKDEV","USE_INFO_1","USE_INFO_1 structure [Network Management]","USE_IPC","USE_NETERR","USE_OK","USE_PAUSED","USE_RECONN","USE_SESSLOST","USE_SPOOLDEV","USE_WILDCARD","_win32_use_info_1_str","lmuse/LPUSE_INFO_1","lmuse/PUSE_INFO_1","lmuse/USE_INFO_1","netmgmt.use_info_1_str"]
old-location: netmgmt\use_info_1_str.htm
tech.root: NetMgmt
ms.assetid: b9f680b8-b56a-42be-9af1-d7b18328ded4
ms.date: 12/05/2018
ms.keywords: '*LPUSE_INFO_1, *PUSE_INFO_1, LPUSE_INFO_1, LPUSE_INFO_1 structure pointer [Network Management], PUSE_INFO_1, PUSE_INFO_1 structure pointer [Network Management], USE_CONN, USE_DISCONN, USE_DISKDEV, USE_INFO_1, USE_INFO_1 structure [Network Management], USE_IPC, USE_NETERR, USE_OK, USE_PAUSED, USE_RECONN, USE_SESSLOST, USE_SPOOLDEV, USE_WILDCARD, _win32_use_info_1_str, lmuse/LPUSE_INFO_1, lmuse/PUSE_INFO_1, lmuse/USE_INFO_1, netmgmt.use_info_1_str'
req.header: lmuse.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: USE_INFO_1, *PUSE_INFO_1, *LPUSE_INFO_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USE_INFO_1
 - lmuse/_USE_INFO_1
 - PUSE_INFO_1
 - lmuse/PUSE_INFO_1
 - USE_INFO_1
 - lmuse/USE_INFO_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmuse.h
api_name:
 - USE_INFO_1
---

# USE_INFO_1 structure


## -description

The
				<b>USE_INFO_1</b> structure contains information about the connection between a local device and a shared resource. The information includes connection status and connection type.

## -struct-fields

### -field ui1_local

Type: <b>LMSTR</b>

A pointer to a string that contains the local device name (for example, drive E or LPT1) being redirected to the shared resource. The constant DEVLEN specifies the maximum number of characters in the string. This member can be <b>NULL</b>. For more information, see the following Remarks section.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field ui1_remote

Type: <b>LMSTR</b>

A pointer to a string that contains the share name of the remote resource being accessed. The string is in the form: 





``` syntax
\\servername\sharename

```

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field ui1_password

Type: <b>LMSTR</b>

A pointer to a string that contains the password needed to establish a session between a specific workstation and a server.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field ui1_status

Type: <b>DWORD</b>

The status of the connection. This element is not used by the 
<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a> function. The following values are defined. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USE_OK"></a><a id="use_ok"></a><dl>
<dt><b>USE_OK</b></dt>
</dl>
</td>
<td width="60%">
The connection is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_PAUSED"></a><a id="use_paused"></a><dl>
<dt><b>USE_PAUSED</b></dt>
</dl>
</td>
<td width="60%">
Paused by local workstation.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_SESSLOST"></a><a id="use_sesslost"></a><dl>
<dt><b>USE_SESSLOST</b></dt>
</dl>
</td>
<td width="60%">
Disconnected.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_DISCONN"></a><a id="use_disconn"></a><dl>
<dt><b>USE_DISCONN</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_NETERR"></a><a id="use_neterr"></a><dl>
<dt><b>USE_NETERR</b></dt>
</dl>
</td>
<td width="60%">
A network error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_CONN"></a><a id="use_conn"></a><dl>
<dt><b>USE_CONN</b></dt>
</dl>
</td>
<td width="60%">
The connection is being made.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_RECONN"></a><a id="use_reconn"></a><dl>
<dt><b>USE_RECONN</b></dt>
</dl>
</td>
<td width="60%">
Reconnecting.

</td>
</tr>
</table>

### -field ui1_asg_type

Type: <b>DWORD</b>

The type of remote resource being accessed. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USE_WILDCARD"></a><a id="use_wildcard"></a><dl>
<dt><b>USE_WILDCARD</b></dt>
</dl>
</td>
<td width="60%">
Matches the type of the server's shared resources. Wildcards can be used only with the 
<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a> function, and only when the <b>ui1_local</b> member is <b>NULL</b>. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_DISKDEV"></a><a id="use_diskdev"></a><dl>
<dt><b>USE_DISKDEV</b></dt>
</dl>
</td>
<td width="60%">
Disk device.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_SPOOLDEV"></a><a id="use_spooldev"></a><dl>
<dt><b>USE_SPOOLDEV</b></dt>
</dl>
</td>
<td width="60%">
Spooled printer.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_IPC"></a><a id="use_ipc"></a><dl>
<dt><b>USE_IPC</b></dt>
</dl>
</td>
<td width="60%">
Interprocess communication (IPC).

</td>
</tr>
</table>

### -field ui1_refcount

Type: <b>DWORD</b>

The number of files, directories, and other processes that are open on the remote resource. This element is not used by the 
<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a> function.

### -field ui1_usecount

Type: <b>DWORD</b>

The number of  explicit connections (redirection with a local device name) or implicit UNC connections (redirection without a local device name) that are established with the resource.

## -remarks

Specifying a <b>ui1_local</b> member that is <b>NULL</b> requests authentication with the server without redirecting a drive letter or a device. Future redirections involving the server while the same connection is in effect use the password specified by the <b>ui1_password</b> member in the initial call to the 
<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a> function.

## -see-also

<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseadd">NetUseAdd</a>



<a href="/windows/desktop/api/lmuse/nf-lmuse-netuseenum">NetUseEnum</a>



<a href="/windows/desktop/api/lmuse/nf-lmuse-netusegetinfo">NetUseGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/use-functions">Use Functions</a>
