---
UID: NS:lmshare._SHARE_INFO_502
title: "_SHARE_INFO_502"
author: windows-sdk-content
description: Contains information about the shared resource, including name of the resource, type and permissions, number of connections, and other pertinent information.
old-location: fs\share_info_502_str.htm
old-project: netshare
ms.assetid: 306e6704-2068-42da-bcc4-c0772c719ee8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPSHARE_INFO_502, *PSHARE_INFO_502, ACCESS_ALL, ACCESS_ATRIB, ACCESS_CREATE, ACCESS_DELETE, ACCESS_EXEC, ACCESS_PERM, ACCESS_READ, ACCESS_WRITE, LPSHARE_INFO_502, LPSHARE_INFO_502 structure pointer [Files], PSHARE_INFO_502, PSHARE_INFO_502 structure pointer [Files], SHARE_INFO_502, SHARE_INFO_502 structure [Files], STYPE_DEVICE, STYPE_DISKTREE, STYPE_IPC, STYPE_PRINTQ, STYPE_SPECIAL, STYPE_TEMPORARY, _SHARE_INFO_502, _win32_share_info_502_str, fs.share_info_502_str, lmshare/LPSHARE_INFO_502, lmshare/PSHARE_INFO_502, lmshare/SHARE_INFO_502, netmgmt.share_info_502_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmshare.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: SHARE_INFO_502, *PSHARE_INFO_502, *LPSHARE_INFO_502
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmshare.h
api_name:
 - SHARE_INFO_502
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SHARE_INFO_502 structure


## -description


Contains information about the shared resource, including name of the resource, type and permissions, number of connections, and other pertinent information.


## -struct-fields




### -field shi502_netname

Pointer to a Unicode string specifying the name of a shared resource. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi502_type

A combination of values that specify the type of share. Calls to the 
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
Disk Drive.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_PRINTQ"></a><a id="stype_printq"></a><dl>
<dt><b>STYPE_PRINTQ</b></dt>
</dl>
</td>
<td width="60%">
Print Queue.

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
Special share reserved for interprocess communication (IPC$) or remote administration of the server (ADMIN$). Can also refer to administrative shares such as C$, D$, E$, and so forth. For more information, see the network 
<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">share functions</a>.

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
 


### -field shi502_remark

Pointer to a Unicode string specifying an optional comment about the shared resource.


### -field shi502_permissions

Specifies a DWORD value that indicates the shared resource's permissions for servers running with share-level security. This member is ignored on a server running user-level security. This member can be any of the following values. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member. 




Note that Windows does not support share-level security. For more information about controlling access to securable objects, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>, <a href="https://msdn.microsoft.com/fe6aae0f-93eb-4aba-a6ac-45e71c251c51">Privileges</a>, and <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">Securable Objects</a>.

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
 


### -field shi502_max_uses

Specifies a DWORD value that indicates the maximum number of concurrent connections that the shared resource can accommodate. The number of connections is unlimited if the value specified in this member is –1.


### -field shi502_current_uses

Specifies a DWORD value that indicates the number of current connections to the resource. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi502_path

Pointer to a Unicode string that contains the local path for the shared resource. For disks, this member is the path being shared. For print queues, this member is the name of the print queue being shared. Calls to the 
<b>NetShareSetInfo</b> function ignore this member.


### -field shi502_passwd

Pointer to a Unicode string that specifies the share's password (when the server is running with share-level security). If the server is running with user-level security, this member is ignored. Note that Windows does not support share-level security. 




This member can be no longer than SHPWLEN+1 bytes (including a terminating null character). Calls to the 
<b>NetShareSetInfo</b> function ignore this member.


### -field shi502_reserved

Reserved; must be zero. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi502_security_descriptor

Specifies the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> associated with this share.


## -see-also




<a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a>



<a href="https://msdn.microsoft.com/9114c54d-3905-4d40-9162-b3ea605f6fcb">NetShareEnum</a>



<a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>



<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

