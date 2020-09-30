---
UID: NF:lmshare.NetShareDel
title: NetShareDel function (lmshare.h)
description: Deletes a share name from a server's list of shared resources, disconnecting all connections to the shared resource.
helpviewer_keywords: ["NetShareDel","NetShareDel function [Files]","_win32_netsharedel","fs.netsharedel","lmshare/NetShareDel","netmgmt.netsharedel"]
old-location: fs\netsharedel.htm
tech.root: fs
ms.assetid: 374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c
ms.date: 12/05/2018
ms.keywords: NetShareDel, NetShareDel function [Files], _win32_netsharedel, fs.netsharedel, lmshare/NetShareDel, netmgmt.netsharedel
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
 - NetShareDel
 - lmshare/NetShareDel
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
 - NetShareDel
---

# NetShareDel function


## -description

Deletes a share name from a server's list of shared resources, disconnecting all connections to the shared resource.

The extended function <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a> allows the caller  to specify a <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>, or <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure.

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

This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="/windows/desktop/WNet/windows-networking-functions">Windows Networking (WNet) functions</a>, which support all types of shares.

Only members of the Administrators, Server Operators, or Power Users local group, or those with Server Operator group membership, can successfully delete file shares with a call to the 
<b>NetShareDel</b> function. The Print Operator can delete printer shares.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileshare">IADsFileShare</a>.


#### Examples

The following code sample demonstrates how to delete a share using a call to the <b>NetShareDel</b> function.


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

   if(argc<3)
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

```

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedelex">NetShareDelEx</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>