---
UID: NS:lmshare._SHARE_INFO_2
title: SHARE_INFO_2 (lmshare.h)
description: Contains information about the shared resource, including name of the resource, type and permissions, and the number of current connections.
helpviewer_keywords: ["*LPSHARE_INFO_2","*PSHARE_INFO_2","ACCESS_ALL","ACCESS_ATRIB","ACCESS_CREATE","ACCESS_DELETE","ACCESS_EXEC","ACCESS_PERM","ACCESS_READ","ACCESS_WRITE","LPSHARE_INFO_2","LPSHARE_INFO_2 structure pointer [Files]","PSHARE_INFO_2","PSHARE_INFO_2 structure pointer [Files]","SHARE_INFO_2","SHARE_INFO_2 structure [Files]","STYPE_DEVICE","STYPE_DISKTREE","STYPE_IPC","STYPE_PRINTQ","STYPE_SPECIAL","STYPE_TEMPORARY","_win32_share_info_2_str","fs.share_info_2_str","lmshare/LPSHARE_INFO_2","lmshare/PSHARE_INFO_2","lmshare/SHARE_INFO_2","netmgmt.share_info_2_str"]
old-location: fs\share_info_2_str.htm
tech.root: fs
ms.assetid: cd152ccd-cd60-455f-b25c-c4939c65e0ab
ms.date: 12/05/2018
ms.keywords: '*LPSHARE_INFO_2, *PSHARE_INFO_2, ACCESS_ALL, ACCESS_ATRIB, ACCESS_CREATE, ACCESS_DELETE, ACCESS_EXEC, ACCESS_PERM, ACCESS_READ, ACCESS_WRITE, LPSHARE_INFO_2, LPSHARE_INFO_2 structure pointer [Files], PSHARE_INFO_2, PSHARE_INFO_2 structure pointer [Files], SHARE_INFO_2, SHARE_INFO_2 structure [Files], STYPE_DEVICE, STYPE_DISKTREE, STYPE_IPC, STYPE_PRINTQ, STYPE_SPECIAL, STYPE_TEMPORARY, _win32_share_info_2_str, fs.share_info_2_str, lmshare/LPSHARE_INFO_2, lmshare/PSHARE_INFO_2, lmshare/SHARE_INFO_2, netmgmt.share_info_2_str'
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
req.typenames: SHARE_INFO_2, *PSHARE_INFO_2, *LPSHARE_INFO_2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHARE_INFO_2
 - lmshare/_SHARE_INFO_2
 - PSHARE_INFO_2
 - lmshare/PSHARE_INFO_2
 - SHARE_INFO_2
 - lmshare/SHARE_INFO_2
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
 - SHARE_INFO_2
---

# SHARE_INFO_2 structure


## -description

Contains information about the shared resource, including name of the resource, type and permissions, and the number of current connections. For more information about controlling access to securable objects, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>, <a href="/windows/desktop/SecAuthZ/privileges">Privileges</a>, and <a href="/windows/desktop/SecAuthZ/securable-objects">Securable Objects</a>.

## -struct-fields

### -field shi2_netname

Pointer to a Unicode string specifying the share name of a resource. Calls to the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a> function ignore this member.

### -field shi2_type

A combination of values that specify the type of the shared resource. Calls to the 
<b>NetShareSetInfo</b> function ignore this member. 



One of the following values may be specified. You can isolate these values by using the <b>STYPE_MASK</b> value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STYPE_DISKTREE"></a><a id="stype_disktree"></a><dl>
<dt><b>STYPE_DISKTREE</b></dt>
</dl>
</td>
<td width="60%">
Disk drive.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_PRINTQ"></a><a id="stype_printq"></a><dl>
<dt><b>STYPE_PRINTQ</b></dt>
</dl>
</td>
<td width="60%">
Print queue.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_DEVICE"></a><a id="stype_device"></a><dl>
<dt><b>STYPE_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
Communication device.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_IPC"></a><a id="stype_ipc"></a><dl>
<dt><b>STYPE_IPC</b></dt>
</dl>
</td>
<td width="60%">
Interprocess communication (IPC).

</td>
</tr>
</table>
 

In addition, one or both of the following values may be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STYPE_SPECIAL"></a><a id="stype_special"></a><dl>
<dt><b>STYPE_SPECIAL</b></dt>
</dl>
</td>
<td width="60%">
Special share reserved for interprocess communication (IPC$) or remote administration of the server (ADMIN$). Can also refer to administrative shares such as C$, D$, E$, and so forth. For more information, see <a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_TEMPORARY"></a><a id="stype_temporary"></a><dl>
<dt><b>STYPE_TEMPORARY</b></dt>
</dl>
</td>
<td width="60%">
A temporary share.

</td>
</tr>
</table>

### -field shi2_remark

Pointer to a Unicode string that contains an optional comment about the shared resource.

### -field shi2_permissions

Specifies a DWORD value that indicates the shared resource's permissions for servers running with share-level security. A server running user-level security ignores this member. This member can be one or more of the following values. Calls to the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a> function ignore this member. 




Note that Windows does not support share-level security.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_READ"></a><a id="access_read"></a><dl>
<dt><b>ACCESS_READ</b></dt>
</dl>
</td>
<td width="60%">
Permission to read data from a resource and, by default, to execute the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_WRITE"></a><a id="access_write"></a><dl>
<dt><b>ACCESS_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Permission to write data to the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_CREATE"></a><a id="access_create"></a><dl>
<dt><b>ACCESS_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Permission to create an instance of the resource (such as a file); data can be written to the resource as the resource is created.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_EXEC"></a><a id="access_exec"></a><dl>
<dt><b>ACCESS_EXEC</b></dt>
</dl>
</td>
<td width="60%">
Permission to execute the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DELETE"></a><a id="access_delete"></a><dl>
<dt><b>ACCESS_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Permission to delete the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ATRIB"></a><a id="access_atrib"></a><dl>
<dt><b>ACCESS_ATRIB</b></dt>
</dl>
</td>
<td width="60%">
Permission to modify the resource's attributes (such as the date and time when a file was last modified).

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_PERM"></a><a id="access_perm"></a><dl>
<dt><b>ACCESS_PERM</b></dt>
</dl>
</td>
<td width="60%">
Permission to modify the permissions (read, write, create, execute, and delete) assigned to a resource for a user or application.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALL"></a><a id="access_all"></a><dl>
<dt><b>ACCESS_ALL</b></dt>
</dl>
</td>
<td width="60%">
Permission to read, write, create, execute, and delete resources, and to modify their attributes and permissions.

</td>
</tr>
</table>

### -field shi2_max_uses

Specifies a DWORD value that indicates the maximum number of concurrent connections that the shared resource can accommodate. The number of connections is unlimited if the value specified in this member is –1.

### -field shi2_current_uses

Specifies a DWORD value that indicates the number of current connections to the resource. Calls to the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a> function ignore this member.

### -field shi2_path

Pointer to a Unicode string specifying the local path for the shared resource. For disks, <b>shi2_path</b> is the path being shared. For print queues, <b>shi2_path</b> is the name of the print queue being shared. Calls to the 
<b>NetShareSetInfo</b> function ignore this member.

### -field shi2_passwd

Pointer to a Unicode string that specifies the share's password when the server is running with share-level security. If the server is running with user-level security, this member is ignored. The <b>shi2_passwd</b> member can be no longer than SHPWLEN+1 bytes (including a terminating null character). Calls to the 
<b>NetShareSetInfo</b> function ignore this member. Note that Windows does not support share-level security.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareenum">NetShareEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>