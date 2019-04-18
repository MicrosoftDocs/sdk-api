---
UID: NF:lmdfs.NetDfsRemove
title: NetDfsRemove function (lmdfs.h)
author: windows-sdk-content
description: Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace. When removing a specific link target, the link itself is removed if the last link target of the link is removed.
old-location: dfs\netdfsremove.htm
tech.root: Dfs
ms.assetid: c879ba56-cc42-4fa3-960f-ddc65a75dbe3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NetDfsRemove, NetDfsRemove function [Distributed File System], _win32_netdfsremove, dfs.netdfsremove, fs.netdfsremove, lmdfs/NetDfsRemove, netmgmt.netdfsremove
ms.topic: function
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - NetDfsRemove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetDfsRemove function


## -description


Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS 
    namespace. When removing a specific link target, the link itself is removed if the last link target of the link is 
    removed.


## -parameters




### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of the DFS link.

The string can be in one of two forms. The first form is as follows:

\\<i>ShareName</i>\<i>DfsName</i>\<i>link_path</i>

where <i>ShareName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

\\<i>DomainName</i>\<i>DomDfsname</i>\<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace; <i>DomDfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

This parameter is required.


### -param ServerName [in, optional]

Pointer to a string that specifies the server name of the link target. For more information, see the 
      following Remarks section. Set this parameter to <b>NULL</b> if the link and all link targets 
      are to be removed.


### -param ShareName [in, optional]

Pointer to a string that specifies the share name of the link target. Set this parameter to 
      <b>NULL</b> if the link and all link targets are to be removed.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller must have Administrator privilege on the DFS server. For more information about calling functions 
    that require administrator privileges, see 
    <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

When you call <b>NetDfsRemove</b> to remove a target from a 
    link, you must specify the same target server name in the <i>ServerName</i> parameter that you 
    specified when you created the link. For example, if you specified the target server's DNS name when you added the 
    target to the link, you must specify the same DNS name when you remove the link. You cannot specify the NetBIOS 
    name.


#### Examples

The following code sample demonstrates how to remove a target from a DFS link using a call to the 
     <b>NetDfsRemove</b> function.


```cpp
#include <windows.h>
#include <lm.h>
#include <lmdfs.h>
#include <stdio.h>
#pragma comment(lib, "Netapi32.lib")

void wmain(int argc, wchar_t *argv[])
{
   DWORD res;
   //
   // All parameters are required.
   //
   if (argc < 4)
      wprintf(L"Syntax: %s DfsEntryPath ServerName ShareName\n", argv[0]);
   else
   {
      //
      // Call the NetDfsRemove function 
      //  to remove the DFS link.
      //
      res = NetDfsRemove(argv[1], argv[2], argv[3]);
      //
      // Display the result of the call.
      //
      if(res == 0)
         printf("Removed DFS link\n");
      else
         printf("Error: %u\n", res);
   }
   return;
}

```





## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/2c8816b2-5489-486e-b749-605932ba9fe9">NetDfsAdd</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/aa5c9991-ca8e-48ba-922d-feadaff45cc2">NetDfsRemoveFtRoot</a>



<a href="https://msdn.microsoft.com/850427cc-56da-45cc-8833-e242acc53589">NetDfsRemoveStdRoot</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>
 

 

