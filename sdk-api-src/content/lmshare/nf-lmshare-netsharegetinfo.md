---
UID: NF:lmshare.NetShareGetInfo
title: NetShareGetInfo function (lmshare.h)
description: Retrieves information about a particular shared resource on a server.
helpviewer_keywords: ["0","1","1005","2","501","502","503","NetShareGetInfo","NetShareGetInfo function [Files]","_win32_netsharegetinfo","fs.netsharegetinfo","lmshare/NetShareGetInfo","netmgmt.netsharegetinfo"]
old-location: fs\netsharegetinfo.htm
tech.root: fs
ms.assetid: 672ea208-4048-4d2f-9606-ee3e2133765b
ms.date: 12/05/2018
ms.keywords: 0, 1, 1005, 2, 501, 502, 503, NetShareGetInfo, NetShareGetInfo function [Files], _win32_netsharegetinfo, fs.netsharegetinfo, lmshare/NetShareGetInfo, netmgmt.netsharegetinfo
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetShareGetInfo
 - lmshare/NetShareGetInfo
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
 - NetShareGetInfo
---

# NetShareGetInfo function


## -description

Retrieves information about a particular shared resource on a server.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param netname [in]

Pointer to a string that specifies the name of the share for which to return information.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
 Return the share name. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
 Return information about the shared resource, including the name and type of the resource, and a comment associated with the resource. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
 Return information about the shared resource, including name of the resource, type and permissions, password, and number of connections. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="501"></a><dl>
<dt><b>501</b></dt>
</dl>
</td>
<td width="60%">
 Return the name and type of the resource, and a comment associated with the resource. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_501">SHARE_INFO_501</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
 Return information about the shared resource, including name of the resource, type and permissions, number of connections, and other pertinent information. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure. If the <b>shi503_servername</b> member of this structure is "*", there is no configured server name.

<b>Windows Server 2003 and Windows XP:  </b>This information level is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
 Return a value that indicates whether the share is the root volume in a Dfs tree structure. The <i>bufptr</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> structure.

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>. 




This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

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
The value specified for the <i>level</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter is not valid.

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
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NetNameNotFound</b></dt>
</dl>
</td>
<td width="60%">
The share name does not exist.

</td>
</tr>
</table>

## -remarks

This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="/windows/desktop/WNet/windows-networking-functions">Windows Networking (WNet) functions</a>, which support all types of shares.

For interactive users (users who are logged on locally to the machine), no special group membership is required to execute the <b>NetShareGetInfo</b> function. For non-interactive users, Administrator, Power User, Print Operator, or Server Operator group membership is required to successfully execute the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareenum">NetShareEnum</a> function at levels 2, 502, and 503. No special group membership is required for level 0 or level 1 calls.

<b>Windows Server 2003 and Windows XP:  </b>For all users, Administrator, Power User, Print Operator, or Server Operator group membership is required to successfully execute the 
<b>NetShareGetInfo</b> function at levels 2 and 502.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileshare">IADsFileShare</a>.

If 503 is specified for the <i>level</i> parameter, the remote server specified in the <b>shi503_servername</b> member of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure must have been bound to a transport protocol using the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.


#### Examples

The following code sample demonstrates how to retrieve information about a particular shared resource using a call to the 
<b>NetShareGetInfo</b> function. The sample calls 
<b>NetShareGetInfo</b>, specifying information level 502 (
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>). If the call succeeds, the code prints the retrieved data. The sample also calls the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a> function to validate the <b>shi502_security_descriptor</b> member. Finally, the sample frees the memory allocated for the information buffer.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include <lm.h>

#pragma comment(lib, "Netapi32.lib")
#pragma comment(lib, "Advapi32.lib")

void wmain( int argc, TCHAR *lpszArgv[ ])
{
   PSHARE_INFO_502 BufPtr;
   NET_API_STATUS res;
   LPTSTR   lpszServer = NULL, lpszShare;
   //
   // Check command line arguments.
   //
   switch(argc)
   {
   case 3:
      lpszServer = lpszArgv[2];
   case 2:
      lpszShare = lpszArgv[1];
      break;
   default:
      printf("Usage: NetShareGetInfo sharename <servername>\n");
      return;
   }
   //
   // Call the NetShareGetInfo function, specifying level 502.
   //
   if((res = NetShareGetInfo (lpszServer,lpszShare,502,(LPBYTE *) &BufPtr)) == ERROR_SUCCESS)
   {
      //
      // Print the retrieved data.
      //
      printf("%S\t%S\t%u\n",BufPtr->shi502_netname, BufPtr->shi502_path, BufPtr->shi502_current_uses);
      //
      // Validate the value of the 
      //  shi502_security_descriptor member.
      //
      if (IsValidSecurityDescriptor(BufPtr->shi502_security_descriptor))
         printf("It has a valid Security Descriptor.\n");
      else
         printf("It does not have a valid Security Descriptor.\n");
      //
      // Free the allocated memory.
      //
      NetApiBufferFree(BufPtr);
   }
   else 
      printf("Error: %ld\n",res);
   return;
}

```

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_501">SHARE_INFO_501</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a>