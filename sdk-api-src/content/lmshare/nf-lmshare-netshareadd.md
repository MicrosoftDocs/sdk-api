---
UID: NF:lmshare.NetShareAdd
title: NetShareAdd function
author: windows-sdk-content
description: Shares a server resource.
old-location: fs\netshareadd.htm
old-project: netshare
ms.assetid: 8b51c155-24e8-4d39-b818-eb2d1bb0ee8b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 2, 502, 503, NetShareAdd, NetShareAdd function [Files], _win32_netshareadd, fs.netshareadd, lmshare/NetShareAdd, netmgmt.netshareadd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmshare.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: SERVER_TRANSPORT_INFO_3, *PSERVER_TRANSPORT_INFO_3, *LPSERVER_TRANSPORT_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetShareAdd
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetShareAdd function


## -description


Shares a server resource.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, and number of connections. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a> structure.

</td>
</tr>
</table>
 


### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


### -param parm_err [out]

Pointer to a value that receives the index of the first member of the share information structure that causes the <b>ERROR_INVALID_PARAMETER</b> error. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the 
<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> function.


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
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The character or file system name is not valid.

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
<dt><b>NERR_DuplicateShare</b></dt>
</dl>
</td>
<td width="60%">
The share name is already in use on this server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_RedirectedPath</b></dt>
</dl>
</td>
<td width="60%">
The operation is not valid for a redirected resource. The specified device name is assigned to a shared resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UnknownDevDir</b></dt>
</dl>
</td>
<td width="60%">
The device or directory does not exist.

</td>
</tr>
</table>
 




## -remarks



This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows Networking (WNet) functions</a>, which support all types of shares.

Only members of the Administrators, System Operators, or Power Users local group can add file shares with a call to the 
<b>NetShareAdd</b> function. The Print Operator can add printer shares.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="https://msdn.microsoft.com/37695195-fc33-499d-98c1-ccfd190cb2f9">IADsFileShare</a>.

If 503 is specified for the <i>level</i> parameter, the remote server specified in the <b>shi503_servername</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a> structure must have been bound to a transport protocol using the <a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.


#### Examples

The following code sample demonstrates how to share a network resource using a call to the 
<b>NetShareAdd</b> function. The code sample fills in the members of the 
<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a> structure and calls 
<b>NetShareAdd</b>, specifying information level 2. A password is not required because these platforms do not support share-level security.


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
   NET_API_STATUS res;
   SHARE_INFO_2 p;
   DWORD parm_err = 0;

   if(argc<2)
      printf("Usage: NetShareAdd server\n");
   else
   {
      //
      // Fill in the SHARE_INFO_2 structure.
      //
      p.shi2_netname = TEXT("TESTSHARE");    
      p.shi2_type = STYPE_DISKTREE; // disk drive
      p.shi2_remark = TEXT("TESTSHARE to test NetShareAdd");
      p.shi2_permissions = 0;    
      p.shi2_max_uses = 4;
      p.shi2_current_uses = 0;    
      p.shi2_path = TEXT("C:\\");
      p.shi2_passwd = NULL; // no password
      //
      // Call the NetShareAdd function,
      //  specifying level 2.
      //
      res=NetShareAdd(argv[1], 2, (LPBYTE) &p, &parm_err);
      //
      // If the call succeeds, inform the user.
      //
      if(res==0)
         printf("Share created.\n");
      
      // Otherwise, print an error,
      //  and identify the parameter in error.
      //
      else
         printf("Error: %u\tparmerr=%u\n", res, parm_err);
   }
   return;
}

```





## -see-also




<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c">NetShareDel</a>



<a href="https://msdn.microsoft.com/2461c533-351b-48f4-b660-cb17ac3398fa">NetShareDelEx</a>



<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>



<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>



<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a>
 

 

