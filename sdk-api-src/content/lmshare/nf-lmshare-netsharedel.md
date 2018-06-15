---
UID: NF:lmshare.NetShareDel
title: NetShareDel function
author: windows-sdk-content
description: Deletes a share name from a server's list of shared resources, disconnecting all connections to the shared resource.
old-location: fs\netsharedel.htm
old-project: NetShare
ms.assetid: 374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: NetShareDel, NetShareDel function [Files], _win32_netsharedel, fs.netsharedel, lmshare/NetShareDel, netmgmt.netsharedel
ms.prod: windows
ms.technology: windows-sdk
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
 - NetShareDel
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetShareDel function


## -description


Deletes a share name from a server's list of shared resources, disconnecting all connections to the shared resource.

The extended function <a href="https://msdn.microsoft.com/2461c533-351b-48f4-b660-cb17ac3398fa">NetShareDelEx</a> allows the caller  to specify a <a href="https://msdn.microsoft.com/47a74c71-1fcb-4c49-93b5-ea7cf3a0e567">SHARE_INFO_0</a>, <a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a>, <a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>, <a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/lmshare/ns-lmshare-_share_info_503">SHARE_INFO_503</a> structure.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.


### -param netname [in]

Pointer to a string that specifies the name of the share to delete.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.


### -param reserved

Reserved, must be zero.


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



This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows Networking (WNet) functions</a>, which support all types of shares.

Only members of the Administrators, Server Operators, or Power Users local group, or those with Server Operator group membership, can successfully delete file shares with a call to the 
<b>NetShareDel</b> function. The Print Operator can delete printer shares.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="https://msdn.microsoft.com/37695195-fc33-499d-98c1-ccfd190cb2f9">IADsFileShare</a>.


#### Examples

The following code sample demonstrates how to delete a share using a call to the <b>NetShareDel</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;lm.h&gt;
#pragma comment(lib, "Netapi32.lib")

void wmain( int argc, TCHAR *argv[ ])
{
   NET_API_STATUS res;

   if(argc&lt;3)
      printf("Usage: NetShareDel server share\n");
   else
   {
      //
      // Call the NetShareDel function to delete the share.
      //
      res=NetShareDel(argv[1], argv[2], 0);
      //
      // Display the result of the call.
      //
      if(res==0)
         printf("Share Removed.\n");
      else
         printf("Error: %u\n", res);
   }
   return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a>



<a href="https://msdn.microsoft.com/2461c533-351b-48f4-b660-cb17ac3398fa">NetShareDelEx</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>
 

 

