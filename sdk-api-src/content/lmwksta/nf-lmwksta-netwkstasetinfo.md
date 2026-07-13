---
UID: NF:lmwksta.NetWkstaSetInfo
title: NetWkstaSetInfo function (lmwksta.h)
description: The NetWkstaSetInfo function configures a workstation with information that remains in effect after the system has been reinitialized.
helpviewer_keywords: ["100","101","102","502","NetWkstaSetInfo","NetWkstaSetInfo function [Network Management]","_win32_netwkstasetinfo","lmwksta/NetWkstaSetInfo","netmgmt.netwkstasetinfo"]
old-location: netmgmt\netwkstasetinfo.htm
tech.root: NetMgmt
ms.assetid: d746b6c9-5ef1-4174-a84f-44e4e50200cd
ms.date: 12/05/2018
ms.keywords: 100, 101, 102, 502, NetWkstaSetInfo, NetWkstaSetInfo function [Network Management], _win32_netwkstasetinfo, lmwksta/NetWkstaSetInfo, netmgmt.netwkstasetinfo
req.header: lmwksta.h
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
 - NetWkstaSetInfo
 - lmwksta/NetWkstaSetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetWkstaSetInfo
---

# NetWkstaSetInfo function


## -description

 The <b>NetWkstaSetInfo</b> function configures a workstation with information  that remains in effect after the system has been reinitialized.

## -parameters

### -param servername [in]

A pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param level [in]

The information level of the data. This parameter can be one of the following values. 



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
<b>Windows NT:  </b>Specifies information about a workstation environment, including platform-specific information, the names of the domain and the local computer, and information concerning the operating system. The <i>buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100">WKSTA_INFO_100</a> structure. The <b>wk100_computername</b> and <b>wk100_langroup</b> fields of this structure cannot be set by calling this function. To set these values, call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a>/<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> or <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain">NetJoinDomain</a>, respectively.

</td>
</tr>
<tr>
<td width="40%"><a id="101"></a><dl>
<dt><b>101</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>In addition to level 100 information, specifies the path to the LANMAN directory. The <i>buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_101">WKSTA_INFO_101</a> structure. The <b>wk101_computername</b> and <b>wk101_langroup</b> fields of this structure cannot be set by calling this function. To set these values, call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a>/<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> or <b>NetJoinDomain</b>, respectively.

</td>
</tr>
<tr>
<td width="40%"><a id="102"></a><dl>
<dt><b>102</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>In addition to level 101 information, specifies the number of users who are logged on to the local computer. The <i>buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_102">WKSTA_INFO_102</a> structure. The <b>wk102_computername</b> and <b>wk102_langroup</b> fields of this structure cannot be set by calling this function. To set these values, call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a>/<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> or <b>NetJoinDomain</b>, respectively.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>The <i>buffer</i> parameter points to a 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_502">WKSTA_INFO_502</a> structure that contains information about the workstation environment.

</td>
</tr>
</table>
 

Do not set levels 1010-1013, 1018, 1023, 1027, 1028, 1032, 1033, 1035, or 1041-1062.

### -param buffer [in]

A pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

A pointer to a value that receives the index of the first member of the workstation information structure that causes the ERROR_INVALID_PARAMETER error. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the Remarks section.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid. For more information, see the following Remarks section.

</td>
</tr>
</table>

## -remarks

Only members of the Administrators group can successfully execute the 
<b>NetWkstaSetInfo</b> function on a remote server.

The
				<b>NetWkstaSetInfo</b> function calls the workstation service on the local system or a remote system. Only a limited number of members of the <a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_502">WKSTA_INFO_502</a> structure can actually be changed using the <b>NetWkstaSetInfo</b> function. No errors are returned if a member is set that is ignored by the workstation service. The workstation service is primarily configured using settings in the registry. 

The <a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausersetinfo">NetWkstaUserSetInfo</a> function can be used instead of the <b>NetWkstaSetInfo</b> function to set configuration information on the local system. The <b>NetWkstaUserSetInfo</b> function calls the Local Security Authority (LSA). 

If the 
<b>NetWkstaSetInfo</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>parm_err</i> parameter to indicate the first member of the workstation information structure that is invalid. (A workstation information structure begins with WKSTA_INFO_ and its format is specified by the <i>level</i> parameter.) The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. (The prefix wki*_ indicates that the member can begin with multiple prefixes, for example, wki100_ or wki402_.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>WKSTA_PLATFORM_ID_PARMNUM</td>
<td>wki*_platform_id</td>
</tr>
<tr>
<td>WKSTA_COMPUTERNAME_PARMNUM</td>
<td>wki*_computername</td>
</tr>
<tr>
<td>WKSTA_LANGROUP_PARMNUM</td>
<td>wki*_langroup</td>
</tr>
<tr>
<td>WKSTA_VER_MAJOR_PARMNUM</td>
<td>wki*_ver_major</td>
</tr>
<tr>
<td>WKSTA_VER_MINOR_PARMNUM</td>
<td>wki*_ver_minor</td>
</tr>
<tr>
<td>WKSTA_LOGGED_ON_USERS_PARMNUM</td>
<td>wki*_logged_on_users</td>
</tr>
<tr>
<td>WKSTA_LANROOT_PARMNUM</td>
<td>wki*_lanroot</td>
</tr>
<tr>
<td>WKSTA_LOGON_DOMAIN_PARMNUM</td>
<td>wki*_logon_domain</td>
</tr>
<tr>
<td>WKSTA_LOGON_SERVER_PARMNUM</td>
<td>wki*_logon_server</td>
</tr>
<tr>
<td>WKSTA_CHARWAIT_PARMNUM</td>
<td>wki*_char_wait</td>
</tr>
<tr>
<td>WKSTA_CHARTIME_PARMNUM</td>
<td>wki*_collection_time</td>
</tr>
<tr>
<td>WKSTA_CHARCOUNT_PARMNUM</td>
<td>wki*_maximum_collection_count</td>
</tr>
<tr>
<td>WKSTA_KEEPCONN_PARMNUM</td>
<td>wki*_keep_conn</td>
</tr>
<tr>
<td>WKSTA_KEEPSEARCH_PARMNUM</td>
<td>wki*_keep_search</td>
</tr>
<tr>
<td>WKSTA_MAXCMDS_PARMNUM</td>
<td>wki*_max_cmds</td>
</tr>
<tr>
<td>WKSTA_NUMWORKBUF_PARMNUM</td>
<td>wki*_num_work_buf</td>
</tr>
<tr>
<td>WKSTA_MAXWRKCACHE_PARMNUM</td>
<td>wki*_max_wrk_cache</td>
</tr>
<tr>
<td>WKSTA_SESSTIMEOUT_PARMNUM</td>
<td>wki*_sess_timeout</td>
</tr>
<tr>
<td>WKSTA_SIZERROR_PARMNUM</td>
<td>wki*_siz_error</td>
</tr>
<tr>
<td>WKSTA_NUMALERTS_PARMNUM</td>
<td>wki*_num_alerts</td>
</tr>
<tr>
<td>WKSTA_NUMSERVICES_PARMNUM</td>
<td>wki*_num_services</td>
</tr>
<tr>
<td>WKSTA_ERRLOGSZ_PARMNUM</td>
<td>wki*_errlog_sz</td>
</tr>
<tr>
<td>WKSTA_PRINTBUFTIME_PARMNUM</td>
<td>wki*_print_buf_time</td>
</tr>
<tr>
<td>WKSTA_NUMCHARBUF_PARMNU</td>
<td>wki*_num_char_buf</td>
</tr>
<tr>
<td>WKSTA_SIZCHARBUF_PARMNUM</td>
<td>wki*_siz_char_buf</td>
</tr>
<tr>
<td>WKSTA_WRKHEURISTICS_PARMNUM</td>
<td>wki*_wrk_heuristics</td>
</tr>
<tr>
<td>WKSTA_MAILSLOTS_PARMNUM</td>
<td>wki*_mailslots</td>
</tr>
<tr>
<td>WKSTA_MAXTHREADS_PARMNUM</td>
<td>wki*_max_threads</td>
</tr>
<tr>
<td>WKSTA_SIZWORKBUF_PARMNUM</td>
<td>wki*_siz_work_buf</td>
</tr>
<tr>
<td>WKSTA_NUMDGRAMBUF_PARMNUM</td>
<td>wki*_num_dgram_buf</td>
</tr>
</table>
 

The workstation service parameter settings are stored in the registry, not in the LanMan.ini file used previously by LAN Manager. The 
<b>NetWkstaSetInfo</b> function does not change the values in the LanMan.ini file. When the workstation service is stopped and restarted, workstation parameters are reset to the default values specified in the registry (unless they are overwritten by command-line parameters). Values set by previous calls to 
<b>NetWkstaSetInfo</b> can be overwritten when workstation parameters are reset.


#### Examples

The following code sample demonstrates how to set the session time-out value associated with a workstation using a call to the 
<b>NetServerSetInfo</b> function. (The session time-out is the number of seconds the server waits before disconnecting an inactive session.) The code specifies information level 502 (<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_502">WKSTA_INFO_502</a>).


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <windows.h> 
#include <lm.h>

int wmain(int argc, wchar_t *argv[])
{
   LPWKSTA_INFO_502 pBuf = NULL;
   WKSTA_INFO_502 wi;
   DWORD dwLevel = 502;
   NET_API_STATUS nStatus;
   LPWSTR pszServerName = NULL;

   if ((argc < 2) || (argc > 3))
   {
      fwprintf(stderr, L"Usage: %s [\\\\ServerName] SessionTimeOut\n", argv[0]);
      exit(1);
   }

   if (argc == 3)
      pszServerName = argv[1];
   //
   // Retrieve the current settings.
   //
   nStatus = NetWkstaGetInfo(pszServerName,
                             dwLevel,
                             (LPBYTE *)&pBuf);

   if (nStatus != NERR_Success)
   {
      fprintf(stderr, "A system error has occurred (NetWkstaGetInfo): %d\n", nStatus);
      return -1;
   }

   if (pBuf != NULL)
   {
      //
      // Copy the existing settings to the new structure,
      //   and free the buffer.
      //
      CopyMemory(&wi, pBuf, sizeof(wi));
      NetApiBufferFree(pBuf);
   }
   else
   {
      fprintf(stderr, "Memory invalid!\n");
      return -1;
   }
   //
   // Set a new session time-out value by
   //   calling the NetWkstaSetInfo function.
   //
   wi.wki502_sess_timeout = _wtoi(argv[argc-1]);
   nStatus = NetWkstaSetInfo(pszServerName,
                             dwLevel,
                             (LPBYTE)&wi,
                             NULL);
   //
   // Display the result of the call.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"Workstation information reset: session time-out = %d\n", _wtoi(argv[argc-1]));
   else
      fprintf(stderr, "A system error has occurred (NetWkstaSetInfo): %d\n", nStatus);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstagetinfo">NetWkstaGetInfo</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausergetinfo">NetWkstaUserGetInfo</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausersetinfo">NetWkstaUserSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/workstation-and-workstation-user-functions">Workstation and Workstation User Functions</a>