---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SESSION_INFO_502 structure


## -description


Contains information about the session, including name of the computer; name of the user; open files, pipes, and devices on the computer; and the name of the transport the client is using.


## -struct-fields




### -field sesi502_cname

Pointer to a Unicode string specifying the name of the computer that established the session. This string cannot contain a backslash (\).


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




<a href="https://msdn.microsoft.com/5923a8cc-bf7a-4ffa-b089-fd7f26ee42d2">NetSessionEnum</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/931455e3-1301-4a68-93c3-2674b3d4c491">Session Functions</a>
 

 

