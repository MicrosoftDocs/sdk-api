---
UID: NF:lmserver.NetServerEnum
title: NetServerEnum function (lmserver.h)
description: The NetServerEnum function lists all servers of the specified type that are visible in a domain.
helpviewer_keywords: ["100","101","NetServerEnum","NetServerEnum function [Network Management]","SV_TYPE_AFP","SV_TYPE_ALL","SV_TYPE_ALTERNATE_XPORT","SV_TYPE_BACKUP_BROWSER","SV_TYPE_CLUSTER_NT","SV_TYPE_CLUSTER_VS_NT","SV_TYPE_DCE","SV_TYPE_DFS","SV_TYPE_DIALIN_SERVER","SV_TYPE_DOMAIN_BAKCTRL","SV_TYPE_DOMAIN_CTRL","SV_TYPE_DOMAIN_ENUM","SV_TYPE_DOMAIN_MASTER","SV_TYPE_DOMAIN_MEMBER","SV_TYPE_LOCAL_LIST_ONLY","SV_TYPE_MASTER_BROWSER","SV_TYPE_NOVELL","SV_TYPE_NT","SV_TYPE_POTENTIAL_BROWSER","SV_TYPE_PRINTQ_SERVER","SV_TYPE_SERVER","SV_TYPE_SERVER_MFPN","SV_TYPE_SERVER_NT","SV_TYPE_SERVER_OSF","SV_TYPE_SERVER_UNIX","SV_TYPE_SERVER_VMS","SV_TYPE_SQLSERVER","SV_TYPE_TERMINALSERVER","SV_TYPE_TIME_SOURCE","SV_TYPE_WFW","SV_TYPE_WINDOWS","SV_TYPE_WORKSTATION","SV_TYPE_XENIX_SERVER","_win32_netserverenum","lmserver/NetServerEnum","netmgmt.netserverenum"]
old-location: netmgmt\netserverenum.htm
tech.root: NetMgmt
ms.assetid: 10012a87-805e-4817-9f09-9e5632b1fa09
ms.date: 12/05/2018
ms.keywords: 100, 101, NetServerEnum, NetServerEnum function [Network Management], SV_TYPE_AFP, SV_TYPE_ALL, SV_TYPE_ALTERNATE_XPORT, SV_TYPE_BACKUP_BROWSER, SV_TYPE_CLUSTER_NT, SV_TYPE_CLUSTER_VS_NT, SV_TYPE_DCE, SV_TYPE_DFS, SV_TYPE_DIALIN_SERVER, SV_TYPE_DOMAIN_BAKCTRL, SV_TYPE_DOMAIN_CTRL, SV_TYPE_DOMAIN_ENUM, SV_TYPE_DOMAIN_MASTER, SV_TYPE_DOMAIN_MEMBER, SV_TYPE_LOCAL_LIST_ONLY, SV_TYPE_MASTER_BROWSER, SV_TYPE_NOVELL, SV_TYPE_NT, SV_TYPE_POTENTIAL_BROWSER, SV_TYPE_PRINTQ_SERVER, SV_TYPE_SERVER, SV_TYPE_SERVER_MFPN, SV_TYPE_SERVER_NT, SV_TYPE_SERVER_OSF, SV_TYPE_SERVER_UNIX, SV_TYPE_SERVER_VMS, SV_TYPE_SQLSERVER, SV_TYPE_TERMINALSERVER, SV_TYPE_TIME_SOURCE, SV_TYPE_WFW, SV_TYPE_WINDOWS, SV_TYPE_WORKSTATION, SV_TYPE_XENIX_SERVER, _win32_netserverenum, lmserver/NetServerEnum, netmgmt.netserverenum
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetServerEnum
 - lmserver/NetServerEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - browcli.dll
 - Ext-MS-Win-SMBShare-BrowserClient-L1-1-0.dll
api_name:
 - NetServerEnum
---

# NetServerEnum function


## -description

The
				<b>NetServerEnum</b> function lists all servers of the specified type that are visible in a domain.

## -parameters

### -param servername [in, optional]

Reserved; must be <b>NULL</b>.

### -param level [in]

The information level of the data requested. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="100"></a><dl>
<dt><b>100</b></dt>
</dl>
</td>
<td width="60%">
Return server names and platform information. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_100">SERVER_INFO_100</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="101"></a><dl>
<dt><b>101</b></dt>
</dl>
</td>
<td width="60%">
Return server names, types, and associated data. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_101">SERVER_INFO_101</a> structures.

</td>
</tr>
</table>

### -param bufptr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.

### -param prefmaxlen [in]

The preferred maximum length of returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param entriesread [out]

A pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

A pointer to a value that receives the total number of visible servers and workstations on the network. Note that applications should consider this value only as a hint.

### -param servertype [in]

A value that filters the server entries to return from the enumeration. This parameter can be a combination of the following values defined in the <i>Lmserver.h</i> header file.

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
All workstations.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER"></a><a id="sv_type_server"></a><dl>
<dt><b>SV_TYPE_SERVER</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
All computers that run the Server service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SQLSERVER"></a><a id="sv_type_sqlserver"></a><dl>
<dt><b>SV_TYPE_SQLSERVER</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Any server that runs an instance of Microsoft SQL Server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_CTRL"></a><a id="sv_type_domain_ctrl"></a><dl>
<dt><b>SV_TYPE_DOMAIN_CTRL</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
A server that is primary domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_BAKCTRL"></a><a id="sv_type_domain_bakctrl"></a><dl>
<dt><b>SV_TYPE_DOMAIN_BAKCTRL</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Any server that is a  backup domain controller.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_TIME_SOURCE"></a><a id="sv_type_time_source"></a><dl>
<dt><b>SV_TYPE_TIME_SOURCE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Any server that runs the Timesource service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_AFP"></a><a id="sv_type_afp"></a><dl>
<dt><b>SV_TYPE_AFP</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Any server that runs the Apple Filing Protocol (AFP) file service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_NOVELL"></a><a id="sv_type_novell"></a><dl>
<dt><b>SV_TYPE_NOVELL</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Any server that is a Novell server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_MEMBER"></a><a id="sv_type_domain_member"></a><dl>
<dt><b>SV_TYPE_DOMAIN_MEMBER</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Any computer that is LAN Manager 2.x domain member.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_PRINTQ_SERVER"></a><a id="sv_type_printq_server"></a><dl>
<dt><b>SV_TYPE_PRINTQ_SERVER</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Any computer that shares a print queue.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DIALIN_SERVER"></a><a id="sv_type_dialin_server"></a><dl>
<dt><b>SV_TYPE_DIALIN_SERVER</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Any server that runs a dial-in service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_XENIX_SERVER"></a><a id="sv_type_xenix_server"></a><dl>
<dt><b>SV_TYPE_XENIX_SERVER</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Any server that is a Xenix server.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_UNIX"></a><a id="sv_type_server_unix"></a><dl>
<dt><b>SV_TYPE_SERVER_UNIX</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Any server that is a UNIX server. This is the same as the <b>SV_TYPE_XENIX_SERVER</b>.

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
Any computer that runs Windows for Workgroups.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_MFPN"></a><a id="sv_type_server_mfpn"></a><dl>
<dt><b>SV_TYPE_SERVER_MFPN</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Any server that runs the Microsoft File and Print for NetWare service.

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
Any computer that can run the browser service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_BACKUP_BROWSER"></a><a id="sv_type_backup_browser"></a><dl>
<dt><b>SV_TYPE_BACKUP_BROWSER</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
A computer that runs a browser service as backup.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_MASTER_BROWSER"></a><a id="sv_type_master_browser"></a><dl>
<dt><b>SV_TYPE_MASTER_BROWSER</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
A computer that runs the master browser service.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_MASTER"></a><a id="sv_type_domain_master"></a><dl>
<dt><b>SV_TYPE_DOMAIN_MASTER</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
A computer that runs the domain master browser.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_OSF"></a><a id="sv_type_server_osf"></a><dl>
<dt><b>SV_TYPE_SERVER_OSF</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
A computer that runs OSF/1.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_SERVER_VMS"></a><a id="sv_type_server_vms"></a><dl>
<dt><b>SV_TYPE_SERVER_VMS</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
A computer that runs Open Virtual Memory System (VMS).

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
A computer that is the root of Distributed File System (DFS) tree.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_CLUSTER_NT"></a><a id="sv_type_cluster_nt"></a><dl>
<dt><b>SV_TYPE_CLUSTER_NT</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Server clusters available in the domain.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_TERMINALSERVER"></a><a id="sv_type_terminalserver"></a><dl>
<dt><b>SV_TYPE_TERMINALSERVER</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
A server running the Terminal Server service.

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
A computer that runs  IBM Directory and Security Services (DSS) or equivalent.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_ALTERNATE_XPORT"></a><a id="sv_type_alternate_xport"></a><dl>
<dt><b>SV_TYPE_ALTERNATE_XPORT</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
A computer that over an alternate transport.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_LOCAL_LIST_ONLY"></a><a id="sv_type_local_list_only"></a><dl>
<dt><b>SV_TYPE_LOCAL_LIST_ONLY</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Any computer maintained in a list by the browser. See the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_DOMAIN_ENUM"></a><a id="sv_type_domain_enum"></a><dl>
<dt><b>SV_TYPE_DOMAIN_ENUM</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
The primary domain.

</td>
</tr>
<tr>
<td width="40%"><a id="SV_TYPE_ALL"></a><a id="sv_type_all"></a><dl>
<dt><b>SV_TYPE_ALL</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
All servers. This is a convenience that will return all possible servers.

</td>
</tr>
</table>

### -param domain [in, optional]

A pointer to a constant string that specifies the name of the domain for which a list of servers is to be returned. The domain name must be a NetBIOS domain name (for example, microsoft). 
The <b>NetServerEnum</b> function does not support DNS-style names (for example, microsoft.com). 

If this parameter is <b>NULL</b>, the primary domain is implied.

### -param resume_handle [in, out, optional]

Reserved; must be set to zero.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Access was denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87</dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234</dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_BROWSER_SERVERS_FOUND</b></dt>
<dt>6118</dt>
</dl>
</td>
<td width="60%">
No browser servers found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
<dt>50</dt>
</dl>
</td>
<td width="60%">
The request is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_RemoteErr</b></dt>
<dt>2127</dt>
</dl>
</td>
<td width="60%">
A remote error occurred with no data returned by the server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_ServerNotStarted</b></dt>
<dt>2114</dt>
</dl>
</td>
<td width="60%">
The server service is not started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_ServiceNotInstalled</b></dt>
<dt>2184</dt>
</dl>
</td>
<td width="60%">
The service has not been started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_WkstaNotStarted</b></dt>
<dt>2138</dt>
</dl>
</td>
<td width="60%">
The Workstation service has not been started. The local workstation service is used  to communicate with a downlevel remote server.

</td>
</tr>
</table>

## -remarks

The
				<b>NetServerEnum</b> function is used to list all servers of the specified type that are visible in a domain. For example, an application can call 
<b>NetServerEnum</b> to list all domain controllers only or all servers that run instances of SQL server only.

An application combine the bit masks for various server types in the <i>servertype</i> parameter to list several types. For example, a value of SV_TYPE_WORKSTATION | SVTYPE_SERVER (0x00000003) combines the bit masks for SV_TYPE_WORKSTATION (0x00000001) and SV_TYPE_SERVER (0x00000002).

If you require more information for a specific server, call the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a> function.

No special group membership is required to successfully execute the 
<b>NetServerEnum</b> function.

If you specify the value SV_TYPE_LOCAL_LIST_ONLY, the 
<b>NetServerEnum</b> function returns the list of servers that the browser maintains internally. This has meaning only on the master browser (or on a computer that has been the master browser in the past). The master browser is the computer that currently has rights to determine which computers can be servers or workstations on the network.

If there are no servers found that match the types specified in the <i>servertype</i> parameter, the 
<b>NetServerEnum</b> function returns the <i>bufptr</i> parameter as <b>NULL</b> and DWORD values pointed to by the <i>entriesread</i> and <i>totalentries</i> parameters are set to zero.

The 
<b>NetServerEnum</b> function depends on the browser service being installed and running. If no browser servers are found, then <b>NetServerEnum</b> fails with ERROR_NO_BROWSER_SERVERS_FOUND.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same function you can achieve by calling the network management server functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>.


#### Examples

The following code sample demonstrates how to list all servers that are visible in a  domain with a call to the 
<b>NetServerEnum</b> function. The sample calls 
<b>NetServerEnum</b>, specifying information level 101 (
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_101">SERVER_INFO_101</a>). If any servers are found, the sample code loops through the entries and prints the retrieved data. If the server is a domain controller, it identifies the server as either a primary domain controller (PDC) or a backup domain controller (BDC). The sample also prints the total number of entries available and a hint about the number of entries actually enumerated, warning the user if all entries were not enumerated. Finally, the sample frees the memory allocated for the information buffer.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <assert.h>
#include <windows.h>
#include <lm.h>

int wmain(int argc, wchar_t * argv[])
{
    LPSERVER_INFO_101 pBuf = NULL;
    LPSERVER_INFO_101 pTmpBuf;
    DWORD dwLevel = 101;
    DWORD dwPrefMaxLen = MAX_PREFERRED_LENGTH;
    DWORD dwEntriesRead = 0;
    DWORD dwTotalEntries = 0;
    DWORD dwTotalCount = 0;
    DWORD dwServerType = SV_TYPE_SERVER;        // all servers
    DWORD dwResumeHandle = 0;
    NET_API_STATUS nStatus;
    LPWSTR pszServerName = NULL;
    LPWSTR pszDomainName = NULL;
    DWORD i;

    if (argc > 2) 
    {
        fwprintf(stderr, L"Usage: %s [DomainName]\n", argv[0]);
        exit(1);
    }
    // The request is not for the primary domain.
    //
    if (argc == 2)
        pszDomainName = argv[1];
    //
    // Call the NetServerEnum function to retrieve information
    //  for all servers, specifying information level 101.
    //
    nStatus = NetServerEnum(pszServerName,
                            dwLevel,
                            (LPBYTE *) & pBuf,
                            dwPrefMaxLen,
                            &dwEntriesRead,
                            &dwTotalEntries,
                            dwServerType, 
                            pszDomainName, 
                            &dwResumeHandle);
    //
    // If the call succeeds,
    //
    if ((nStatus == NERR_Success) || (nStatus == ERROR_MORE_DATA)) {
        if ((pTmpBuf = pBuf) != NULL) {
            //
            // Loop through the entries and 
            //  print the data for all server types.
            //
            for (i = 0; i < dwEntriesRead; i++) {
                assert(pTmpBuf != NULL);

                if (pTmpBuf == NULL) {
                    fprintf(stderr, "An access violation has occurred\n");
                    break;
                }

                printf("\tPlatform: %d\n", pTmpBuf->sv101_platform_id);
                wprintf(L"\tName:     %s\n", pTmpBuf->sv101_name);
                printf("\tVersion:  %d.%d\n",
                       pTmpBuf->sv101_version_major,
                       pTmpBuf->sv101_version_minor);
                printf("\tType:     %d", pTmpBuf->sv101_type);
                //
                // Check to see if the server is a domain controller;
                //  if so, identify it as a PDC or a BDC.
                //
                if (pTmpBuf->sv101_type & SV_TYPE_DOMAIN_CTRL)
                    wprintf(L" (PDC)");
                else if (pTmpBuf->sv101_type & SV_TYPE_DOMAIN_BAKCTRL)
                    wprintf(L" (BDC)");

                printf("\n");
                //
                // Also print the comment associated with the server.
                //
                wprintf(L"\tComment:  %s\n\n", pTmpBuf->sv101_comment);

                pTmpBuf++;
                dwTotalCount++;
            }
            // Display a warning if all available entries were
            //  not enumerated, print the number actually 
            //  enumerated, and the total number available.

            if (nStatus == ERROR_MORE_DATA) {
                fprintf(stderr, "\nMore entries available!!!\n");
                fprintf(stderr, "Total entries: %d", dwTotalEntries);
            }

            printf("\nEntries enumerated: %d\n", dwTotalCount);

        } else {
            printf("No servers were found\n");
            printf("The buffer (bufptr) returned was NULL\n");
            printf("  entriesread: %d\n", dwEntriesRead);
            printf("  totalentries: %d\n", dwEntriesRead);
        }

    } else
        fprintf(stderr, "NetServerEnum failed with error: %d\n", nStatus);
    //
    // Free the allocated buffer.
    //
    if (pBuf != NULL)
        NetApiBufferFree(pBuf);

    return 0;
}


```

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netserverdiskenum">NetServerDiskEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_100">SERVER_INFO_100</a>



<a href="/windows/desktop/api/lmserver/ns-lmserver-server_info_101">SERVER_INFO_101</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server
		  Functions</a>