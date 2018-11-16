---
UID: NS:lmserver._SERVER_INFO_403
title: "_SERVER_INFO_403"
author: windows-sdk-content
description: The SERVER_INFO_403 structure contains information about a specified server.
old-location: netmgmt\server_info_403_str.htm
tech.root: NetMgmt
ms.assetid: 14309dbe-ad7b-4ae0-8acc-39e9999f411b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPSERVER_INFO_403, *PSERVER_INFO_403, LPSERVER_INFO_403, LPSERVER_INFO_403 structure pointer [Network Management], PSERVER_INFO_403, PSERVER_INFO_403 structure pointer [Network Management], SERVER_INFO_403, SERVER_INFO_403 structure [Network Management], SV_SHARESECURITY, SV_USERSECURITY, SW_AUTOPROF_LOAD_MASK, SW_AUTOPROF_SAVE_MASK, _SERVER_INFO_403, _win32_server_info_403_str, lmserver/LPSERVER_INFO_403, lmserver/PSERVER_INFO_403, lmserver/SERVER_INFO_403, netmgmt.server_info_403_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: lmserver.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_403
product: Windows
targetos: Windows
req.typenames: SERVER_INFO_403, *PSERVER_INFO_403, *LPSERVER_INFO_403
req.redist: 
---

# _SERVER_INFO_403 structure


## -description


The
				<b>SERVER_INFO_403</b> structure contains information about a specified server.


## -struct-fields




### -field sv403_ulist_mtime

Type: <b>DWORD</b>

The last time the user list was modified. The value is expressed as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT, and applies to servers running with user-level security.


### -field sv403_glist_mtime

Type: <b>DWORD</b>

The last time the group list was modified. The value is expressed as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT, and applies to servers running with user-level security.


### -field sv403_alist_mtime

Type: <b>DWORD</b>

The last time the access control list was modified. The value is expressed as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT, and applies to servers running with user-level security.


### -field sv403_alerts

Type: <b>LMSTR</b>

A pointer to a string that specifies the list of user names on the server. Spaces separate the names.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field sv403_security

Type: <b>DWORD</b>

The security type of the server. This member can be one of the following values. Note that Windows NT, Windows 2000, Windows XP, and Windows Server 2003 operating systems do not support share-level security. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SV_SHARESECURITY"></a><a id="sv_sharesecurity"></a><dl>
<dt><b>SV_SHARESECURITY</b></dt>
</dl>
</td>
<td width="60%">
Share-level security

</td>
</tr>
<tr>
<td width="40%"><a id="SV_USERSECURITY"></a><a id="sv_usersecurity"></a><dl>
<dt><b>SV_USERSECURITY</b></dt>
</dl>
</td>
<td width="60%">
User-level security

</td>
</tr>
</table>
 


### -field sv403_numadmin

Type: <b>DWORD</b>

The number of administrators the server can accommodate at one time.


### -field sv403_lanmask

Type: <b>DWORD</b>

The order in which the network device drivers are served.


### -field sv403_guestacct

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of a reserved account for guest users on the server. The UNLEN constant specifies the maximum number of characters in the string.


### -field sv403_chdevs

Type: <b>DWORD</b>

The number of character devices that can be shared on the server.


### -field sv403_chdevq

Type: <b>DWORD</b>

The number of character device queues that can coexist on the server.


### -field sv403_chdevjobs

Type: <b>DWORD</b>

The number of character device jobs that can be pending at one time on the server.


### -field sv403_connections

Type: <b>DWORD</b>

The number of connections allowed on the server.


### -field sv403_shares

Type: <b>DWORD</b>

The number of share names the server can accommodate.


### -field sv403_openfiles

Type: <b>DWORD</b>

The number of files that can be open at once on the server.


### -field sv403_sessopens

Type: <b>DWORD</b>

The number of files that one session can open.


### -field sv403_sessvcs

Type: <b>DWORD</b>

The maximum number of virtual circuits permitted per client.


### -field sv403_sessreqs

Type: <b>DWORD</b>

The number of simultaneous requests a client can make on a single virtual circuit.


### -field sv403_opensearch

Type: <b>DWORD</b>

The number of search operations that can be carried out simultaneously.


### -field sv403_activelocks

Type: <b>DWORD</b>

The number of file locks that can be active at the same time.


### -field sv403_numreqbuf

Type: <b>DWORD</b>

The number of server buffers that are provided.


### -field sv403_sizreqbuf

Type: <b>DWORD</b>

The size, in bytes, of each server buffer.


### -field sv403_numbigbuf

Type: <b>DWORD</b>

The number of 64K server buffers provided.


### -field sv403_numfiletasks

Type: <b>DWORD</b>

The number of processes that can access the operating system at the same time.


### -field sv403_alertsched

Type: <b>DWORD</b>

The alert interval, in seconds, for notifying an administrator of a network event.


### -field sv403_erroralert

Type: <b>DWORD</b>

The number of entries that can be written to the error log, in any one interval, before notifying an administrator. The interval is specified by the <b>sv403_alertsched</b> member.


### -field sv403_logonalert

Type: <b>DWORD</b>

The  number of invalid attempts that a user tries to logon before notifying an administrator.


### -field sv403_accessalert

Type: <b>DWORD</b>

The number of invalid file access attempts to allow before notifying an administrator.


### -field sv403_diskalert

Type: <b>DWORD</b>

The amount of free disk space at which the system sends a message notifying an administrator that free space on a disk is low. This value is expressed as the number of kilobytes of free disk space remaining on the disk.


### -field sv403_netioalert

Type: <b>DWORD</b>

The network I/O error ratio, in tenths of a percent, that is allowed before notifying an administrator.


### -field sv403_maxauditsz

Type: <b>DWORD</b>

The maximum audit file size in kilobytes. The audit file traces user activity.


### -field sv403_srvheuristics

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains flags that are used to control operations on a server.


### -field sv403_auditedevents

Type: <b>DWORD</b>

The audit event control mask.


### -field sv403_autoprofile

Type: <b>DWORD</b>

A value that controls the action of the server on the profile. The following values are predefined. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SW_AUTOPROF_LOAD_MASK"></a><a id="sw_autoprof_load_mask"></a><dl>
<dt><b>SW_AUTOPROF_LOAD_MASK</b></dt>
</dl>
</td>
<td width="60%">
The server loads the profile.

</td>
</tr>
<tr>
<td width="40%"><a id="SW_AUTOPROF_SAVE_MASK"></a><a id="sw_autoprof_save_mask"></a><dl>
<dt><b>SW_AUTOPROF_SAVE_MASK</b></dt>
</dl>
</td>
<td width="60%">
The server saves the profile.

</td>
</tr>
</table>
 


### -field sv403_autopath

Type: <b>LPWSTR</b>

A pointer to a Unicode string that contains the path for the profile.


## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/1a04a43d-34f9-4a08-ac66-750120792af0">NetServerSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server Functions</a>
 

 

