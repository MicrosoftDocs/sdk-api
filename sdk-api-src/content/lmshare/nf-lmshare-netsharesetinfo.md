---
UID: NF:lmshare.NetShareSetInfo
title: NetShareSetInfo function
author: windows-sdk-content
description: Sets the parameters of a shared resource.
old-location: fs\netsharesetinfo.htm
tech.root: NetShare
ms.assetid: 216b0b78-87da-4734-ad07-5ad1c9edf494
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 1, 1004, 1005, 1006, 1501, 2, 502, 503, NetShareSetInfo, NetShareSetInfo function [Files], _win32_netsharesetinfo, fs.netsharesetinfo, lmshare/NetShareSetInfo, netmgmt.netsharesetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetShareSetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, password, and number of connections. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name and type of the resource, required permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Specifies the name of the shared resource. The <i>buf</i> parameter points to a <a href="fs.share_info_503">SHARE_INFO_503</a> structure. All members of this structure except <b>shi503_servername</b> are ignored by the <b>NetShareSetInfo</b> function.

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
<a href="https://msdn.microsoft.com/41749066-d0e2-4a6b-aea5-216af9a530f4">SHARE_INFO_1004</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
Specifies a set of flags describing  the shared resource. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1006"></a><dl>
<dt><b>1006</b></dt>
</dl>
</td>
<td width="60%">
Specifies the maximum number of concurrent connections that the shared resource can accommodate. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/645a8670-5661-4d6c-8d9e-67c1bbb0f1d7">SHARE_INFO_1006</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1501"></a><dl>
<dt><b>1501</b></dt>
</dl>
</td>
<td width="60%">
 Specifies the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> associated with the specified share. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/ef5d4936-8c0b-4a3c-b2b9-34868eb01a2e">SHARE_INFO_1501</a> structure.

</td>
</tr>
</table>
 


### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


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



This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows Networking (WNet) functions</a>, which support all types of shares.

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
<a href="https://msdn.microsoft.com/37695195-fc33-499d-98c1-ccfd190cb2f9">IADsFileShare</a>.

If 503 is specified for the <i>level</i> parameter, the remote server specified in the <b>shi503_servername</b> member of the <a href="fs.share_info_503">SHARE_INFO_503</a> structure must have been bound to a transport protocol using the <a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.


#### Examples

The following code sample demonstrates how to set the comment associated with a shared resource using a call to the 
<b>NetShareSetInfo</b> function. To do this, the sample specifies information level 1004 (<a href="https://msdn.microsoft.com/41749066-d0e2-4a6b-aea5-216af9a530f4">SHARE_INFO_1004</a>).


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




<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>



<a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a>



<a href="https://msdn.microsoft.com/41749066-d0e2-4a6b-aea5-216af9a530f4">SHARE_INFO_1004</a>



<a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a>



<a href="https://msdn.microsoft.com/645a8670-5661-4d6c-8d9e-67c1bbb0f1d7">SHARE_INFO_1006</a>



<a href="https://msdn.microsoft.com/ef5d4936-8c0b-4a3c-b2b9-34868eb01a2e">SHARE_INFO_1501</a>



<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>



<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>



<a href="fs.share_info_503">SHARE_INFO_503</a>
 

 

