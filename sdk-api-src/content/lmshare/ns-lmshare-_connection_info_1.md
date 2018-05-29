---
UID: NS:lmshare._CONNECTION_INFO_1
title: "_CONNECTION_INFO_1"
author: windows-sdk-content
description: Contains the identification number of a connection, number of open files, connection time, number of users on the connection, and the type of connection.
old-location: fs\connection_info_1_str.htm
old-project: NetShare
ms.assetid: 9904c448-dcc4-47cc-a2e0-7df8d4d37f3f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*LPCONNECTION_INFO_1, *PCONNECTION_INFO_1, CONNECTION_INFO_1, CONNECTION_INFO_1 structure [Files], LPCONNECTION_INFO_1, LPCONNECTION_INFO_1 structure pointer [Files], PCONNECTION_INFO_1, PCONNECTION_INFO_1 structure pointer [Files], STYPE_DEVICE, STYPE_DISKTREE, STYPE_IPC, STYPE_PRINTQ, STYPE_SPECIAL, STYPE_TEMPORARY, _CONNECTION_INFO_1, _win32_connection_info_1_str, fs.connection_info_1_str, lmshare/CONNECTION_INFO_1, lmshare/LPCONNECTION_INFO_1, lmshare/PCONNECTION_INFO_1, netmgmt.connection_info_1_str"
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
req.typenames: CONNECTION_INFO_1, *PCONNECTION_INFO_1, *LPCONNECTION_INFO_1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Lmshare.h
api_name:
-	CONNECTION_INFO_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _CONNECTION_INFO_1 structure


## -description


Contains the identification number of a connection, number of open files, connection time, number of users on the connection, and the type of connection.


## -struct-fields




### -field coni1_id

Specifies a connection identification number.


### -field coni1_type

A combination of values that specify the type of connection made from the local device name to the shared resource. 

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
Special share reserved for interprocess communication (IPC$) or remote administration of the server (ADMIN$). Can also refer to administrative shares such as C$, D$, E$, and so forth. For more information, see <a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>.

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
 


### -field coni1_num_opens

Specifies the number of files currently open as a result of the connection.


### -field coni1_num_users

Specifies the number of users on the connection.


### -field coni1_time

Specifies the number of seconds that the connection has been established.


### -field coni1_username

Pointer to a string. If the server sharing the resource is running with user-level security, the <b>coni1_username</b> member describes which user made the connection. If the server is running with share-level security, <b>coni1_username</b> describes which computer (computername) made the connection. Note that Windows does not support share-level security.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field coni1_netname

Pointer to a string that specifies either the share name of the server's shared resource or the computername of the client. The value of this member depends on which name was specified as the <i>qualifier</i> parameter to the 
<a href="https://msdn.microsoft.com/935ac6e9-78e0-42ae-a454-0a14b03ddc21">NetConnectionEnum</a> function. The name not specified in the <i>qualifier</i> parameter to 
<b>NetConnectionEnum</b> is automatically supplied to <b>coni1_netname</b>.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -see-also




<a href="https://msdn.microsoft.com/935ac6e9-78e0-42ae-a454-0a14b03ddc21">NetConnectionEnum</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

