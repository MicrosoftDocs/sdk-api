---
UID: NS:lmserver._SERVER_INFO_402
title: SERVER_INFO_402 (lmserver.h)
description: Contains information about a specified server.
helpviewer_keywords: ["*LPSERVER_INFO_402","*PSERVER_INFO_402","LPSERVER_INFO_402","LPSERVER_INFO_402 structure pointer [Network Management]","PSERVER_INFO_402","PSERVER_INFO_402 structure pointer [Network Management]","SERVER_INFO_402","SERVER_INFO_402 structure [Network Management]","SV_SHARESECURITY","SV_USERSECURITY","_win32_server_info_402_str","lmserver/LPSERVER_INFO_402","lmserver/PSERVER_INFO_402","lmserver/SERVER_INFO_402","netmgmt.server_info_402_str"]
old-location: netmgmt\server_info_402_str.htm
tech.root: NetMgmt
ms.assetid: 51e5c27e-6a7d-45ac-9cfa-37b1f7f241f9
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_402, *PSERVER_INFO_402, LPSERVER_INFO_402, LPSERVER_INFO_402 structure pointer [Network Management], PSERVER_INFO_402, PSERVER_INFO_402 structure pointer [Network Management], SERVER_INFO_402, SERVER_INFO_402 structure [Network Management], SV_SHARESECURITY, SV_USERSECURITY, _win32_server_info_402_str, lmserver/LPSERVER_INFO_402, lmserver/PSERVER_INFO_402, lmserver/SERVER_INFO_402, netmgmt.server_info_402_str'
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
targetos: Windows
req.typenames: SERVER_INFO_402, *PSERVER_INFO_402, *LPSERVER_INFO_402
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_402
 - lmserver/_SERVER_INFO_402
 - PSERVER_INFO_402
 - lmserver/PSERVER_INFO_402
 - SERVER_INFO_402
 - lmserver/SERVER_INFO_402
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmserver.h
api_name:
 - SERVER_INFO_402
---

# SERVER_INFO_402 structure


## -description

The
				<b>SERVER_INFO_402</b> structure contains information about a specified server.

## -struct-fields

### -field sv402_ulist_mtime

Type: <b>DWORD</b>

The last time the user list was modified. The value is expressed as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT, and applies to servers running with user-level security.

### -field sv402_glist_mtime

Type: <b>DWORD</b>

The last time the group list was modified. The value is expressed as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT, and applies to servers running with user-level security.

### -field sv402_alist_mtime

Type: <b>DWORD</b>

The last time the access control list was modified. The value is expressed as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT, and applies to servers running with user-level security.

### -field sv402_alerts

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the list of user names on the server. Spaces separate the names.

### -field sv402_security

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

### -field sv402_numadmin

Type: <b>DWORD</b>

The number of administrators the server can accommodate at one time.

### -field sv402_lanmask

Type: <b>DWORD</b>

The order in which the network device drivers are served.

### -field sv402_guestacct

Type: <b>LPWSTR</b>

A pointer to a Unicode string that specifies the name of a reserved account for guest users on the server. The constant UNLEN specifies the maximum number of characters in the string.

### -field sv402_chdevs

Type: <b>DWORD</b>

The number of character-oriented devices that can be shared on the server.

### -field sv402_chdevq

Type: <b>DWORD</b>

The number of character-oriented device queues that can coexist on the server.

### -field sv402_chdevjobs

Type: <b>DWORD</b>

The number of  character-oriented device jobs that can be pending at one time on the server.

### -field sv402_connections

Type: <b>DWORD</b>

The number of connections allowed on the server.

### -field sv402_shares

Type: <b>DWORD</b>

The number of share names the server can accommodate.

### -field sv402_openfiles

Type: <b>DWORD</b>

The number of files that can be open at once on the server.

### -field sv402_sessopens

Type: <b>DWORD</b>

The number of files that one session can open.

### -field sv402_sessvcs

Type: <b>DWORD</b>

The maximum number of virtual circuits permitted per client.

### -field sv402_sessreqs

Type: <b>DWORD</b>

The number of simultaneous requests a client can make on a single virtual circuit.

### -field sv402_opensearch

Type: <b>DWORD</b>

The number of search operations that can be carried out simultaneously.

### -field sv402_activelocks

Type: <b>DWORD</b>

The number of file locks that can be active at the same time.

### -field sv402_numreqbuf

Type: <b>DWORD</b>

The number of server buffers provided.

### -field sv402_sizreqbuf

Type: <b>DWORD</b>

The size, in bytes, of each server buffer.

### -field sv402_numbigbuf

Type: <b>DWORD</b>

The number of 64K server buffers provided.

### -field sv402_numfiletasks

Type: <b>DWORD</b>

The number of processes that can access the operating system at one time.

### -field sv402_alertsched

Type: <b>DWORD</b>

The interval, in seconds, for notifying an administrator of a network event.

### -field sv402_erroralert

Type: <b>DWORD</b>

The number of entries that can be written to the error log, in any one interval, before notifying an administrator. The interval is specified by the <b>sv402_alertsched</b>  member.

### -field sv402_logonalert

Type: <b>DWORD</b>

The number of invalid logon attempts to allow a user before notifying an administrator.

### -field sv402_accessalert

Type: <b>DWORD</b>

The number of invalid file access attempts to allow before notifying an administrator.

### -field sv402_diskalert

Type: <b>DWORD</b>

The point at which the system sends a message notifying an administrator that free space on a disk is low. This value is expressed as the number of kilobytes of free disk space remaining on the disk.

### -field sv402_netioalert

Type: <b>DWORD</b>

The network I/O error ratio, in tenths of a percent, that is allowed before notifying an administrator.

### -field sv402_maxauditsz

Type: <b>DWORD</b>

The maximum size, in kilobytes, of the audit file. The audit file traces user activity.

### -field sv402_srvheuristics

Type: <b>LPWSTR</b>

A pointer to a Unicode string containing flags that control operations on a server.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netserversetinfo">NetServerSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>