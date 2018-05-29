---
UID: NS:lmshare._SHARE_INFO_503
title: "_SHARE_INFO_503"
author: windows-sdk-content
description: Contains information about the shared resource. It is identical to the SHARE_INFO_502 structure, except that it also contains the server name.
old-location: fs\share_info_503_str.htm
old-project: NetShare
ms.assetid: 12650bc0-f67d-464e-8386-a0fd53cdc749
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*LPSHARE_INFO_503, *PSHARE_INFO_503, ACCESS_ALL, ACCESS_ATRIB, ACCESS_CREATE, ACCESS_DELETE, ACCESS_EXEC, ACCESS_PERM, ACCESS_READ, ACCESS_WRITE, LPSHARE_INFO_503, LPSHARE_INFO_503 structure pointer [Files], PSHARE_INFO_503, PSHARE_INFO_503 structure pointer [Files], SHARE_INFO_503, SHARE_INFO_503 structure [Files], STYPE_DEVICE, STYPE_DISKTREE, STYPE_IPC, STYPE_PRINTQ, STYPE_SPECIAL, STYPE_TEMPORARY, _SHARE_INFO_503, fs.share_info_503, fs.share_info_503_str, lmshare/LPSHARE_INFO_503, lmshare/PSHARE_INFO_503, lmshare/SHARE_INFO_503"
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
req.typenames: SHARE_INFO_503, *PSHARE_INFO_503, *LPSHARE_INFO_503
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmshare.h
api_name:
-	SHARE_INFO_503
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _SHARE_INFO_503 structure


## -description


Contains information about the shared resource. It is identical to the <a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a> structure, except that it also contains the server name.


## -struct-fields




### -field shi503_netname

A pointer to a Unicode string specifying the name of a shared resource. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi503_type

A combination of values that specify the type of share. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.

One of the following values may be specified. You can isolate these values by using the <b>STYPE_MASK</b> value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STYPE_DISKTREE"></a><a id="stype_disktree"></a><dl>
<dt><b>STYPE_DISKTREE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Disk drive.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_PRINTQ"></a><a id="stype_printq"></a><dl>
<dt><b>STYPE_PRINTQ</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Print queue.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_DEVICE"></a><a id="stype_device"></a><dl>
<dt><b>STYPE_DEVICE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Communication device.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_IPC"></a><a id="stype_ipc"></a><dl>
<dt><b>STYPE_IPC</b></dt>
<dt>0x00000003</dt>
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
<dt>0x80000000</dt>
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
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
A temporary share.

</td>
</tr>
</table>
 


### -field shi503_remark

A pointer to a Unicode string specifying an optional comment about the shared resource.


### -field shi503_permissions

Specifies a DWORD value that indicates the shared resource's permissions for servers running with share-level security. Note that Windows does not support share-level security. This member is ignored on a server running user-level security. For more information about controlling access to securable objects, see <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">Privileges</a>, and <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">Securable Objects</a>. 






Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.

This member can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_READ"></a><a id="access_read"></a><dl>
<dt><b>ACCESS_READ</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Permission to read data from a resource and, by default, to execute the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_WRITE"></a><a id="access_write"></a><dl>
<dt><b>ACCESS_WRITE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Permission to write data to the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_CREATE"></a><a id="access_create"></a><dl>
<dt><b>ACCESS_CREATE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Permission to create an instance of the resource (such as a file); data can be written to the resource as the resource is created.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_EXEC"></a><a id="access_exec"></a><dl>
<dt><b>ACCESS_EXEC</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Permission to execute the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DELETE"></a><a id="access_delete"></a><dl>
<dt><b>ACCESS_DELETE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Permission to delete the resource.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ATRIB"></a><a id="access_atrib"></a><dl>
<dt><b>ACCESS_ATRIB</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Permission to modify the resource's attributes (such as the date and time when a file was last modified).

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_PERM"></a><a id="access_perm"></a><dl>
<dt><b>ACCESS_PERM</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Permission to modify the permissions (read, write, create, execute, and delete) assigned to a resource for a user or application.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALL"></a><a id="access_all"></a><dl>
<dt><b>ACCESS_ALL</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Permission to read, write, create, execute, and delete resources, and to modify their attributes and permissions.

</td>
</tr>
</table>
 


### -field shi503_max_uses

Specifies a DWORD value that indicates the maximum number of concurrent connections that the shared resource can accommodate. The number of connections is unlimited if the value specified in this member is –1.


### -field shi503_current_uses

Specifies a DWORD value that indicates the number of current connections to the resource. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi503_path

A pointer to a Unicode string that contains the local path for the shared resource. For disks, this member is the path being shared. For print queues, this member is the name of the print queue being shared. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi503_passwd

A pointer to a Unicode string that specifies the share's password (when the server is running with share-level security). If the server is running with user-level security, this member is ignored. Note that Windows does not support share-level security. 




This member can be no longer than SHPWLEN+1 bytes (including a terminating null character). Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi503_servername

A pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the shared resource resides. A value of "*" indicates no configured server name.


### -field shi503_reserved

Reserved; must be zero. Calls to the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function ignore this member.


### -field shi503_security_descriptor

Specifies the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> associated with this share.


## -remarks



The remote server specified in the <b>shi503_servername</b> member must have been bound to a transport protocol using the <a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> value must have been specified in the <a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.




## -see-also




<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/a1360f5d-9fd0-44af-b9f5-ab9bc057dfe6">NetSessionDel</a>



<a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a>



<a href="https://msdn.microsoft.com/2461c533-351b-48f4-b660-cb17ac3398fa">NetShareDelEx</a>



<a href="https://msdn.microsoft.com/9114c54d-3905-4d40-9162-b3ea605f6fcb">NetShareEnum</a>



<a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>



<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

