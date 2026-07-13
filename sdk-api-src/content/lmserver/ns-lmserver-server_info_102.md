---
UID: NS:lmserver._SERVER_INFO_102
title: SERVER_INFO_102 (lmserver.h)
description: Contains information about the specified server, including name, platform, type of server, attributes, and associated software.
helpviewer_keywords: ["*LPSERVER_INFO_102","*PSERVER_INFO_102","LPSERVER_INFO_102","LPSERVER_INFO_102 structure pointer [Network Management]","PLATFORM_ID_DOS","PLATFORM_ID_NT","PLATFORM_ID_OS2","PLATFORM_ID_OSF","PLATFORM_ID_VMS","PSERVER_INFO_102","PSERVER_INFO_102 structure pointer [Network Management]","SERVER_INFO_102","SERVER_INFO_102 structure [Network Management]","SV_HIDDEN","SV_TYPE_AFP","SV_TYPE_ALTERNATE_XPORT","SV_TYPE_BACKUP_BROWSER","SV_TYPE_CLUSTER_NT","SV_TYPE_CLUSTER_VS_NT","SV_TYPE_DCE","SV_TYPE_DFS","SV_TYPE_DIALIN_SERVER","SV_TYPE_DOMAIN_BAKCTRL","SV_TYPE_DOMAIN_CTRL","SV_TYPE_DOMAIN_ENUM","SV_TYPE_DOMAIN_MASTER","SV_TYPE_DOMAIN_MEMBER","SV_TYPE_LOCAL_LIST_ONLY","SV_TYPE_MASTER_BROWSER","SV_TYPE_NOVELL","SV_TYPE_NT","SV_TYPE_POTENTIAL_BROWSER","SV_TYPE_PRINTQ_SERVER","SV_TYPE_SERVER","SV_TYPE_SERVER_MFPN","SV_TYPE_SERVER_NT","SV_TYPE_SERVER_OSF","SV_TYPE_SERVER_VMS","SV_TYPE_SQLSERVER","SV_TYPE_TERMINALSERVER","SV_TYPE_TIME_SOURCE","SV_TYPE_WFW","SV_TYPE_WINDOWS","SV_TYPE_WORKSTATION","SV_TYPE_XENIX_SERVER","SV_VISIBLE","_win32_server_info_102_str","lmserver/LPSERVER_INFO_102","lmserver/PSERVER_INFO_102","lmserver/SERVER_INFO_102","netmgmt.server_info_102_str"]
old-location: netmgmt\server_info_102_str.htm
tech.root: NetMgmt
ms.assetid: 4c63fee7-1103-414d-b650-da87f8184e91
ms.date: 12/05/2018
ms.keywords: '*LPSERVER_INFO_102, *PSERVER_INFO_102, LPSERVER_INFO_102, LPSERVER_INFO_102 structure pointer [Network Management], PLATFORM_ID_DOS, PLATFORM_ID_NT, PLATFORM_ID_OS2, PLATFORM_ID_OSF, PLATFORM_ID_VMS, PSERVER_INFO_102, PSERVER_INFO_102 structure pointer [Network Management], SERVER_INFO_102, SERVER_INFO_102 structure [Network Management], SV_HIDDEN, SV_TYPE_AFP, SV_TYPE_ALTERNATE_XPORT, SV_TYPE_BACKUP_BROWSER, SV_TYPE_CLUSTER_NT, SV_TYPE_CLUSTER_VS_NT, SV_TYPE_DCE, SV_TYPE_DFS, SV_TYPE_DIALIN_SERVER, SV_TYPE_DOMAIN_BAKCTRL, SV_TYPE_DOMAIN_CTRL, SV_TYPE_DOMAIN_ENUM, SV_TYPE_DOMAIN_MASTER, SV_TYPE_DOMAIN_MEMBER, SV_TYPE_LOCAL_LIST_ONLY, SV_TYPE_MASTER_BROWSER, SV_TYPE_NOVELL, SV_TYPE_NT, SV_TYPE_POTENTIAL_BROWSER, SV_TYPE_PRINTQ_SERVER, SV_TYPE_SERVER, SV_TYPE_SERVER_MFPN, SV_TYPE_SERVER_NT, SV_TYPE_SERVER_OSF, SV_TYPE_SERVER_VMS, SV_TYPE_SQLSERVER, SV_TYPE_TERMINALSERVER, SV_TYPE_TIME_SOURCE, SV_TYPE_WFW, SV_TYPE_WINDOWS, SV_TYPE_WORKSTATION, SV_TYPE_XENIX_SERVER, SV_VISIBLE, _win32_server_info_102_str, lmserver/LPSERVER_INFO_102, lmserver/PSERVER_INFO_102, lmserver/SERVER_INFO_102, netmgmt.server_info_102_str'
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
req.typenames: SERVER_INFO_102, *PSERVER_INFO_102, *LPSERVER_INFO_102
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVER_INFO_102
 - lmserver/_SERVER_INFO_102
 - PSERVER_INFO_102
 - lmserver/PSERVER_INFO_102
 - SERVER_INFO_102
 - lmserver/SERVER_INFO_102
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
 - SERVER_INFO_102
---

# SERVER_INFO_102 structure


## -description

The
				<b>SERVER_INFO_102</b> structure contains information about the specified server, including name, platform, type of server, attributes, and associated software.

## -struct-fields

### -field sv102_platform_id

Type: <b>DWORD</b>

The information level to use for platform-specific information.

Possible values for this member are listed in the <i>Lmcons.h</i> header file.


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_DOS"></a><a id="platform_id_dos"></a><dl>
<dt><b>PLATFORM_ID_DOS</b></dt>
<dt>300</dt>
</dl>
</td>
<td width="60%">
The MS-DOS platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_OS2"></a><a id="platform_id_os2"></a><dl>
<dt><b>PLATFORM_ID_OS2</b></dt>
<dt>400</dt>
</dl>
</td>
<td width="60%">
The OS/2 platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_NT"></a><a id="platform_id_nt"></a><dl>
<dt><b>PLATFORM_ID_NT</b></dt>
<dt>500</dt>
</dl>
</td>
<td width="60%">
The Windows NT platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_OSF"></a><a id="platform_id_osf"></a><dl>
<dt><b>PLATFORM_ID_OSF</b></dt>
<dt>600</dt>
</dl>
</td>
<td width="60%">
The OSF platform.

</td>
</tr>
<tr>
<td width="40%"><a id="PLATFORM_ID_VMS"></a><a id="platform_id_vms"></a><dl>
<dt><b>PLATFORM_ID_VMS</b></dt>
<dt>700</dt>
</dl>
</td>
<td width="60%">
The VMS platform.

</td>
</tr>
</table>

### -field sv102_name

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying the name of a server.

### -field sv102_version_major

Type: <b>DWORD</b>

The major version number and the server type. 

The major release version number of the operating system is specified in the least significant 4 bits. The server type is specified in the most significant 4 bits. The <b>MAJOR_VERSION_MASK</b> bitmask defined in the <i>Lmserver.h</i> header should be used by an  application to obtain the major version number from this member.

### -field sv102_version_minor

Type: <b>DWORD</b>

The minor release version number of the operating system.

### -field sv102_type

Type: <b>DWORD</b>

The type of software the computer is running. 

Possible values for this member are listed in the <i>Lmserver.h</i> header file.
This member can be a combination of some of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_WORKSTATION"></a><a id="sv_type_workstation"></a><dl>
<dt><b>SV_TYPE_WORKSTATION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
A workstation.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER"></a><a id="sv_type_server"></a><dl>
<dt><b>SV_TYPE_SERVER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
A server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SQLSERVER"></a><a id="sv_type_sqlserver"></a><dl>
<dt><b>SV_TYPE_SQLSERVER</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
A server running with Microsoft SQL Server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_CTRL"></a><a id="sv_type_domain_ctrl"></a><dl>
<dt><b>SV_TYPE_DOMAIN_CTRL</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
A primary domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_BAKCTRL"></a><a id="sv_type_domain_bakctrl"></a><dl>
<dt><b>SV_TYPE_DOMAIN_BAKCTRL</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
A backup domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_TIME_SOURCE"></a><a id="sv_type_time_source"></a><dl>
<dt><b>SV_TYPE_TIME_SOURCE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
A server running the Timesource service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_AFP"></a><a id="sv_type_afp"></a><dl>
<dt><b>SV_TYPE_AFP</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
A server running the Apple Filing Protocol (AFP) file service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_NOVELL"></a><a id="sv_type_novell"></a><dl>
<dt><b>SV_TYPE_NOVELL</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
A Novell server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_MEMBER"></a><a id="sv_type_domain_member"></a><dl>
<dt><b>SV_TYPE_DOMAIN_MEMBER</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
A LAN Manager 2.x domain member.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_PRINTQ_SERVER"></a><a id="sv_type_printq_server"></a><dl>
<dt><b>SV_TYPE_PRINTQ_SERVER</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
A server that shares a print queue.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DIALIN_SERVER"></a><a id="sv_type_dialin_server"></a><dl>
<dt><b>SV_TYPE_DIALIN_SERVER</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
A server that runs a dial-in service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_XENIX_SERVER"></a><a id="sv_type_xenix_server"></a><dl>
<dt><b>SV_TYPE_XENIX_SERVER</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
A Xenix or Unix server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_NT"></a><a id="sv_type_nt"></a><dl>
<dt><b>SV_TYPE_NT</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
A workstation or server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_WFW"></a><a id="sv_type_wfw"></a><dl>
<dt><b>SV_TYPE_WFW</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
A computer that runs Windows for Workgroups.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_MFPN"></a><a id="sv_type_server_mfpn"></a><dl>
<dt><b>SV_TYPE_SERVER_MFPN</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
A server that runs the Microsoft File and Print for NetWare service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_NT"></a><a id="sv_type_server_nt"></a><dl>
<dt><b>SV_TYPE_SERVER_NT</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Any server that is not a domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_POTENTIAL_BROWSER"></a><a id="sv_type_potential_browser"></a><dl>
<dt><b>SV_TYPE_POTENTIAL_BROWSER</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
A computer that can run the browser service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_BACKUP_BROWSER"></a><a id="sv_type_backup_browser"></a><dl>
<dt><b>SV_TYPE_BACKUP_BROWSER</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
A server running a browser service as backup.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_MASTER_BROWSER"></a><a id="sv_type_master_browser"></a><dl>
<dt><b>SV_TYPE_MASTER_BROWSER</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
A server running the master browser service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_MASTER"></a><a id="sv_type_domain_master"></a><dl>
<dt><b>SV_TYPE_DOMAIN_MASTER</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
A server running the domain master browser.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_OSF"></a><a id="sv_type_server_osf"></a><dl>
<dt><b>SV_TYPE_SERVER_OSF</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
A computer that runs OSF.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_VMS"></a><a id="sv_type_server_vms"></a><dl>
<dt><b>SV_TYPE_SERVER_VMS</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
A computer that runs VMS.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_WINDOWS"></a><a id="sv_type_windows"></a><dl>
<dt><b>SV_TYPE_WINDOWS</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
A computer that runs Windows.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DFS"></a><a id="sv_type_dfs"></a><dl>
<dt><b>SV_TYPE_DFS</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
A server that is the root of  a DFS tree.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_CLUSTER_NT"></a><a id="sv_type_cluster_nt"></a><dl>
<dt><b>SV_TYPE_CLUSTER_NT</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
A server cluster available in the domain.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_TERMINALSERVER"></a><a id="sv_type_terminalserver"></a><dl>
<dt><b>SV_TYPE_TERMINALSERVER</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
A server that runs the Terminal Server service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_CLUSTER_VS_NT"></a><a id="sv_type_cluster_vs_nt"></a><dl>
<dt><b>SV_TYPE_CLUSTER_VS_NT</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
 Cluster virtual servers available in the domain.

<b>Windows 2000:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DCE"></a><a id="sv_type_dce"></a><dl>
<dt><b>SV_TYPE_DCE</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
A server that runs the DCE Directory and Security Services or equivalent.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_ALTERNATE_XPORT"></a><a id="sv_type_alternate_xport"></a><dl>
<dt><b>SV_TYPE_ALTERNATE_XPORT</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
A server that is returned by an alternate transport.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_LOCAL_LIST_ONLY"></a><a id="sv_type_local_list_only"></a><dl>
<dt><b>SV_TYPE_LOCAL_LIST_ONLY</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
A server that is maintained by the browser.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_ENUM"></a><a id="sv_type_domain_enum"></a><dl>
<dt><b>SV_TYPE_DOMAIN_ENUM</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
A primary domain.

</td>
</tr>
</table>
 

The <b>SV_TYPE_ALL</b> constant is defined to 0xFFFFFFFF in the <i>Lmserver.h</i> header file. This constant can be used to check for all server types when used with the <a href="/windows/desktop/api/lmserver/nf-lmserver-netserverenum">NetServerEnum</a> function.

### -field sv102_comment

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying a comment describing the server. The comment can be null.

### -field sv102_users

Type: <b>DWORD</b>

The number of users who can attempt to log on to the system server. Note that it is the license server that determines how many of these users can actually log on.

### -field sv102_disc

Type: <b>LONG</b>

The auto-disconnect time, in minutes. A session is disconnected if it is idle longer than the period of time specified by the <b>sv102_disc</b> member. If the value of <b>sv102_disc</b> is SV_NODISC, auto-disconnect is not enabled.

### -field sv102_hidden

Type: <b>BOOL</b>

A value that indicates whether the server is visible to other computers in the same network domain. This member can be one of the following values defined in the <i>Lmserver.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SV_VISIBLE"></a><a id="sv_visible"></a><dl>
<dt><b>SV_VISIBLE</b></dt>
</dl>
</td>
<td width="60%">
The server is visible.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_HIDDEN"></a><a id="sv_hidden"></a><dl>
<dt><b>SV_HIDDEN</b></dt>
</dl>
</td>
<td width="60%">
The server is not visible.

</td>
</tr>
</table>

### -field sv102_announce

Type: <b>DWORD</b>

The network announce rate, in seconds. This rate determines how often the server is announced to other computers on the network. For more information about how much the announce rate can vary from the period of time specified by this member, see 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_1018">SERVER_INFO_1018</a>.

### -field sv102_anndelta

Type: <b>DWORD</b>

The delta value for the announce rate, in milliseconds. This value specifies how much the announce rate can vary from the period of time specified in the <b>sv102_announce</b> member.

The delta value allows randomly varied announce rates. For example, if the <b>sv102_announce</b> member has the value 10 and the <b>sv102_anndelta</b>  member has the value 1, the announce rate can vary from 9.999 seconds to 10.001 seconds.

### -field sv102_licenses

Type: <b>DWORD</b>

The number of users per license. By default, this number is SV_USERS_PER_LICENSE.

### -field sv102_userpath

Type: <b>LPWSTR</b>

A pointer to a Unicode string specifying the path to user directories.

## -remarks

To retrieve a value that indicates whether a share is the root volume in a Dfs tree structure, you must call the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> function and specify information level 1005.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo">NetServerGetInfo</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netserversetinfo">NetServerSetInfo</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_1018">SERVER_INFO_1018</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server Functions</a>