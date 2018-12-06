---
UID: NF:lmserver.NetServerSetInfo
title: NetServerSetInfo function
author: windows-sdk-content
description: The NetServerSetInfo function sets a server's operating parameters; it can set them individually or collectively. The information is stored in a way that allows it to remain in effect after the system has been reinitialized.
old-location: netmgmt\netserversetinfo.htm
tech.root: netmgmt
ms.assetid: 1a04a43d-34f9-4a08-ac66-750120792af0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 101, 102, 402, 403, NetServerSetInfo, NetServerSetInfo function [Network Management], _win32_netserversetinfo, lmserver/NetServerSetInfo, netmgmt.netserversetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetServerSetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetServerSetInfo function


## -description


The
				<b>NetServerSetInfo</b> function sets a server's operating parameters; it can set them individually or collectively. The information is stored in a way that allows it to remain in effect after the system has been reinitialized.


## -parameters




### -param servername [in]

Pointer to a string that specifies the name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="101"></a><dl>
<dt><b>101</b></dt>
</dl>
</td>
<td width="60%">
Specifies the server name, type, and associated software. The <i>buf</i>  parameter points to a 
<a href="https://msdn.microsoft.com/6e106a51-9f0c-4603-8121-5b0d01a235b4">SERVER_INFO_101</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="102"></a><dl>
<dt><b>102</b></dt>
</dl>
</td>
<td width="60%">
Specifies the server name, type, associated software, and other attributes. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/4c63fee7-1103-414d-b650-da87f8184e91">SERVER_INFO_102</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="402"></a><dl>
<dt><b>402</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the server. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/51e5c27e-6a7d-45ac-9cfa-37b1f7f241f9">SERVER_INFO_402</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="403"></a><dl>
<dt><b>403</b></dt>
</dl>
</td>
<td width="60%">
Specifies detailed information about the server. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/14309dbe-ad7b-4ae0-8acc-39e9999f411b">SERVER_INFO_403</a> structure.

</td>
</tr>
</table>
 

In addition, levels 1001-1006, 1009-1011, 1016-1018, 1021, 1022, 1028, 1029, 1037, and 1043 are valid based on the restrictions for LAN Manager systems.


### -param buf [in]

Pointer to a buffer that receives the server information. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


### -param ParmError [out]

Pointer to a value that receives the index of the first member of the server information structure that causes the ERROR_INVALID_PARAMETER error. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the following Remarks section.


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
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter is invalid. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
</table>
 




## -remarks



Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetServerSetInfo</b> function.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management server functions. For more information, see 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.

If the 
<b>NetServerSetInfo</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>ParmError</i> parameter to indicate the first member of the server information structure that is invalid. (A server information structure begins with SERVER_INFO_ and its format is specified by the <i>level</i> parameter.) The following table lists the values that can be returned in the <i>ParmError</i> parameter and the corresponding structure member that is in error. (The prefix sv*_ indicates that the member can begin with multiple prefixes, for example, sv101_ or sv402_.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>SV_PLATFORM_ID_PARMNUM</td>
<td>sv*_platform_id</td>
</tr>
<tr>
<td>SV_NAME_PARMNUM</td>
<td>sv*_name</td>
</tr>
<tr>
<td>SV_VERSION_MAJOR_PARMNUM</td>
<td>sv*_version_major</td>
</tr>
<tr>
<td>SV_VERSION_MINOR_PARMNUM</td>
<td>sv*_version_minor</td>
</tr>
<tr>
<td>SV_TYPE_PARMNUM</td>
<td>sv*_type</td>
</tr>
<tr>
<td>SV_COMMENT_PARMNUM</td>
<td>sv*_comment</td>
</tr>
<tr>
<td>SV_USERS_PARMNUM</td>
<td>sv*_users</td>
</tr>
<tr>
<td>SV_DISC_PARMNUM</td>
<td>sv*_disc</td>
</tr>
<tr>
<td>SV_HIDDEN_PARMNUM</td>
<td>sv*_hidden</td>
</tr>
<tr>
<td>SV_ANNOUNCE_PARMNUM</td>
<td>sv*_announce</td>
</tr>
<tr>
<td>SV_ANNDELTA_PARMNUM</td>
<td>sv*_anndelta</td>
</tr>
<tr>
<td>SV_USERPATH_PARMNUM</td>
<td>sv*_userpath</td>
</tr>
<tr>
<td>SV_ULIST_MTIME_PARMNUM</td>
<td>sv*_ulist_mtime</td>
</tr>
<tr>
<td>SV_GLIST_MTIME_PARMNUM</td>
<td>sv*_glist_mtime</td>
</tr>
<tr>
<td>SV_ALIST_MTIME_PARMNUM</td>
<td>sv*_alist_mtime</td>
</tr>
<tr>
<td>SV_ALERTS_PARMNUM</td>
<td>sv*_alerts</td>
</tr>
<tr>
<td>SV_SECURITY_PARMNUM</td>
<td>sv*_security</td>
</tr>
<tr>
<td>SV_NUMADMIN_PARMNUM</td>
<td>sv*_numadmin</td>
</tr>
<tr>
<td>SV_LANMASK_PARMNUM</td>
<td>sv*_lanmask</td>
</tr>
<tr>
<td>SV_GUESTACC_PARMNUM</td>
<td>sv*_guestacc</td>
</tr>
<tr>
<td>SV_CHDEVQ_PARMNUM</td>
<td>sv*_chdevq</td>
</tr>
<tr>
<td>SV_CHDEVJOBS_PARMNUM</td>
<td>sv*_chdevjobs</td>
</tr>
<tr>
<td>SV_CONNECTIONS_PARMNUM</td>
<td>sv*_connections</td>
</tr>
<tr>
<td>SV_SHARES_PARMNUM</td>
<td>sv*_shares</td>
</tr>
<tr>
<td>SV_OPENFILES_PARMNUM</td>
<td>sv*_openfiles</td>
</tr>
<tr>
<td>SV_SESSOPENS_PARMNUM</td>
<td>sv*_sessopens</td>
</tr>
<tr>
<td>SV_SESSVCS_PARMNUM</td>
<td>sv*_sessvcs</td>
</tr>
<tr>
<td>SV_SESSREQS_PARMNUM</td>
<td>sv*_sessreqs</td>
</tr>
<tr>
<td>SV_OPENSEARCH_PARMNUM</td>
<td>sv*_opensearch</td>
</tr>
<tr>
<td>SV_ACTIVELOCKS_PARMNUM</td>
<td>sv*_activelocks</td>
</tr>
<tr>
<td>SV_NUMREQBUF_PARMNUM</td>
<td>sv*_numreqbuf</td>
</tr>
<tr>
<td>SV_SIZREQBUF_PARMNUM</td>
<td>sv*_sizreqbuf</td>
</tr>
<tr>
<td>SV_NUMBIGBUF_PARMNUM</td>
<td>sv*_numbigbuf</td>
</tr>
<tr>
<td>SV_NUMFILETASKS_PARMNUM</td>
<td>sv*_numfiletasks</td>
</tr>
<tr>
<td>SV_ALERTSCHED_PARMNUM</td>
<td>sv*_alertsched</td>
</tr>
<tr>
<td>SV_ERRORALERT_PARMNUM</td>
<td>sv*_erroralert</td>
</tr>
<tr>
<td>SV_LOGONALERT_PARMNUM</td>
<td>sv*_logonalert</td>
</tr>
<tr>
<td>SV_ACCESSALERT_PARMNUM</td>
<td>sv*_accessalert</td>
</tr>
<tr>
<td>SV_DISKALERT_PARMNUM</td>
<td>sv*_diskalert</td>
</tr>
<tr>
<td>SV_NETIOALERT_PARMNUM</td>
<td>sv*_netioalert</td>
</tr>
<tr>
<td>SV_MAXAUDITSZ_PARMNUM</td>
<td>sv*_maxauditsz</td>
</tr>
<tr>
<td>SV_SRVHEURISTICS_PARMNUM</td>
<td>sv*_srvheuristics</td>
</tr>
<tr>
<td>SV_TIMESOURCE_PARMNUM</td>
<td>sv*_timesource</td>
</tr>
</table>
 


#### Examples

The following code sample demonstrates how to call the 
<b>NetServerSetInfo</b> function. The sample calls 
<b>NetServerSetInfo</b>, specifying the <i>level</i> parameter as 1005 (required) to set the <b>sv1005_comment</b> member of the <a href="https://msdn.microsoft.com/a8ce88ee-2b44-4b12-ba7a-f84249a3621b">SERVER_INFO_1005</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include &lt;stdio.h&gt;
#include &lt;windows.h&gt; 
#include &lt;lm.h&gt;

int wmain(int argc, wchar_t *argv[])
{
   DWORD dwLevel = 1005;
   SERVER_INFO_1005 si;
   NET_API_STATUS nStatus;

   if (argc != 3)
   {
      fwprintf(stderr, L"Usage: %s \\\\ServerName Comment\n", argv[0]);
      exit(1);
   }
   //
   // Fill in SERVER_INFO_1005 structure member.
   //
   si.sv1005_comment = (LPTSTR) argv[2];
   //
   // Call the NetServerSetInfo function, 
   //  specifying level 1005.
   //
   nStatus = NetServerSetInfo(argv[1],
                              dwLevel,
                              (LPBYTE)&amp;si,
                              NULL);
   //
   // Display the result of the call.
   //
   if (nStatus == NERR_Success)
      fwprintf(stderr, L"Comment reset\n", argv[2]);
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);
   return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ed15e1b5-3fdc-4841-85d1-89269684df0e">NetServerGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/6e106a51-9f0c-4603-8121-5b0d01a235b4">SERVER_INFO_101</a>



<a href="https://msdn.microsoft.com/4c63fee7-1103-414d-b650-da87f8184e91">SERVER_INFO_102</a>



<a href="https://msdn.microsoft.com/51e5c27e-6a7d-45ac-9cfa-37b1f7f241f9">SERVER_INFO_402</a>



<a href="https://msdn.microsoft.com/14309dbe-ad7b-4ae0-8acc-39e9999f411b">SERVER_INFO_403</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server
		  Functions</a>
 

 

