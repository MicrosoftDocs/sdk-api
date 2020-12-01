---
UID: NF:lmshare.NetShareSetInfo
title: NetShareSetInfo function (lmshare.h)
description: Sets the parameters of a shared resource.
helpviewer_keywords: ["1","1004","1005","1006","1501","2","502","503","NetShareSetInfo","NetShareSetInfo function [Files]","_win32_netsharesetinfo","fs.netsharesetinfo","lmshare/NetShareSetInfo","netmgmt.netsharesetinfo"]
old-location: fs\netsharesetinfo.htm
tech.root: fs
ms.assetid: 216b0b78-87da-4734-ad07-5ad1c9edf494
ms.date: 12/05/2018
ms.keywords: 1, 1004, 1005, 1006, 1501, 2, 502, 503, NetShareSetInfo, NetShareSetInfo function [Files], _win32_netsharesetinfo, fs.netsharesetinfo, lmshare/NetShareSetInfo, netmgmt.netsharesetinfo
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
 - NetShareSetInfo
 - lmshare/NetShareSetInfo
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
 - NetShareSetInfo
---

# NetShareSetInfo function


## -description

Sets the parameters of a shared resource.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param netname [in]

Pointer to a string that specifies the name of the share to set information on.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 




<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name and type of the resource, and a comment associated with the resource. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, password, and number of connections. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name and type of the resource, required permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Specifies the name of the shared resource. The <i>buf</i> parameter points to a <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure. All members of this structure except <b>shi503_servername</b> are ignored by the <b>NetShareSetInfo</b> function.

<b>Windows Server 2003 and Windows XP:  </b>This information level is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="1004"></a><dl>
<dt><b>1004</b></dt>
</dl>
</td>
<td width="60%">
Specifies a comment associated with the shared resource. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1004">SHARE_INFO_1004</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
Specifies a set of flags describing  the shared resource. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1006"></a><dl>
<dt><b>1006</b></dt>
</dl>
</td>
<td width="60%">
Specifies the maximum number of concurrent connections that the shared resource can accommodate. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1006">SHARE_INFO_1006</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1501"></a><dl>
<dt><b>1501</b></dt>
</dl>
</td>
<td width="60%">
 Specifies the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> associated with the specified share. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1501">SHARE_INFO_1501</a> structure.

</td>
</tr>
</table>

### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first member of the share information structure that causes the <b>ERROR_INVALID_PARAMETER</b> error. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the following Remarks section.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

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
The specified parameter is not valid. For more information, see the following Remarks section.

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

Only members of the Administrators or Power Users local group, or those with Print or Server Operator group membership, can successfully execute the 
<b>NetShareSetInfo</b> function. The Print Operator can set information only about Printer shares.

If the 
<b>NetShareSetInfo</b> function returns <b>ERROR_INVALID_PARAMETER</b>, you can use the <i>parm_err</i> parameter to indicate the first member of the share information structure that is not valid. (A share information structure begins with <b>SHARE_INFO_</b> and its format is specified by the <i>level</i> parameter.) The following table lists the values that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. (The prefix <b>shi*_</b> indicates that the member can begin with multiple prefixes, for example, <i>shi2_</i> or <b>shi502_</b>.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>SHARE_NETNAME_PARMNUM</td>
<td><b>shi*_netname</b></td>
</tr>
<tr>
<td>SHARE_TYPE_PARMNUM</td>
<td><b>shi*_type</b></td>
</tr>
<tr>
<td>SHARE_REMARK_PARMNUM</td>
<td><b>shi*_remark</b></td>
</tr>
<tr>
<td>SHARE_PERMISSIONS_PARMNUM</td>
<td><b>shi*_permissions</b></td>
</tr>
<tr>
<td>SHARE_MAX_USES_PARMNUM</td>
<td><b>shi*_max_uses</b></td>
</tr>
<tr>
<td>SHARE_CURRENT_USES_PARMNUM</td>
<td><b>shi*_current_uses</b></td>
</tr>
<tr>
<td>SHARE_PATH_PARMNUM</td>
<td><b>shi*_path</b></td>
</tr>
<tr>
<td>SHARE_PASSWD_PARMNUM</td>
<td><b>shi*_passwd</b></td>
</tr>
<tr>
<td>SHARE_FILE_SD_PARMNUM</td>
<td><b>shi*_security_descriptor</b></td>
</tr>
</table>
 

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileshare">IADsFileShare</a>.

If 503 is specified for the <i>level</i> parameter, the remote server specified in the <b>shi503_servername</b> member of the <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure must have been bound to a transport protocol using the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.


#### Examples

The following code sample demonstrates how to set the comment associated with a shared resource using a call to the 
<b>NetShareSetInfo</b> function. To do this, the sample specifies information level 1004 (<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1004">SHARE_INFO_1004</a>).


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include <lm.h>
#pragma comment(lib, "Netapi32.lib")

void wmain( int argc, TCHAR *argv[ ])
{
   SHARE_INFO_1004 p;
   NET_API_STATUS res;
   DWORD parm_err = 0;

   if(argc<4)
      printf("Usage: SetInfo server share \"remark\"\n");
   else
   {
      //
      // Fill in SHARE_INFO_1004 structure member.
      //
      p.shi1004_remark=argv[3];
      //
      // Call the NetShareSetInfo function,
      //  specifying information level 1004.
      //
      res=NetShareSetInfo(argv[1], argv[2], 1004, (LPBYTE)&p, &parm_err);
      //
      // Display the result of the call.
      //
      if(res==0)
         printf("Remark set.\n");
      else
         printf("Error: %u\tparmerr=%u\n", res, parm_err);
   }
   return;
}

```

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1004">SHARE_INFO_1004</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1006">SHARE_INFO_1006</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1501">SHARE_INFO_1501</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a>