---
UID: NF:lmdfs.NetDfsAdd
title: NetDfsAdd function (lmdfs.h)
description: Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.
helpviewer_keywords: ["DFS_ADD_VOLUME","DFS_RESTORE_VOLUME","NetDfsAdd","NetDfsAdd function [Distributed File System]","_win32_netdfsadd","dfs.netdfsadd","fs.netdfsadd","lmdfs/NetDfsAdd","netmgmt.netdfsadd"]
old-location: dfs\netdfsadd.htm
tech.root: Dfs
ms.assetid: 2c8816b2-5489-486e-b749-605932ba9fe9
ms.date: 12/05/2018
ms.keywords: DFS_ADD_VOLUME, DFS_RESTORE_VOLUME, NetDfsAdd, NetDfsAdd function [Distributed File System], _win32_netdfsadd, dfs.netdfsadd, fs.netdfsadd, lmdfs/NetDfsAdd, netmgmt.netdfsadd
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
req.lib: NetApi32.lib
req.dll: NetApi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetDfsAdd
 - lmdfs/NetDfsAdd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NetApi32.dll
api_name:
 - NetDfsAdd
---

# NetDfsAdd function


## -description

Creates a new Distributed File System (DFS) link or adds 
    targets to an existing link in a DFS namespace.

## -parameters

### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS link in a DFS namespace.

The string can be in one of two forms. The first form is as follows:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>&#92;<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts a stand-alone DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>&#92;<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts a domain-based DFS namespace; <i>DomDfsname</i> is the name of 
       the domain-based DFS namespace; and 
       <i>link_path</i> is a DFS link.

This parameter is required.

### -param ServerName [in]

Pointer to a string that specifies the link target server name. This parameter 
      is required.

### -param ShareName [in]

Pointer to a string that specifies the link target share name. This can also be a share name with a path relative to the share. For example, <i>share1\mydir1\mydir2</i>. This parameter is required.

### -param Comment [in, optional]

Pointer to a string that specifies an optional comment associated with the DFS link. This parameter is 
      ignored when the function adds a target to an existing link.

### -param Flags [in]

This parameter can specify the following value, or you can specify zero for no flags.



#### DFS_ADD_VOLUME (0x00000001)

Create a DFS link. If the DFS link already exists, the <b>NetDfsAdd</b> 
        function fails. For more information, see the Remarks section.



#### DFS_RESTORE_VOLUME (0x00000002)

This flag is not supported.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
      <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The DFS namespace must already exist. This function does not create a new DFS namespace.

The caller must have Administrator privilege on the DFS server. For more information about calling functions that require administrator privileges, see 
    <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

Use of the <b>DFS_ADD_VOLUME</b> flag is optional. If you specify 
    <b>DFS_ADD_VOLUME</b> and the link already exists, <b>NetDfsAdd</b> 
    fails. If you do not specify <b>DFS_ADD_VOLUME</b>, 
    <b>NetDfsAdd</b> creates the link, if required, and adds the target to the link. You 
    should specify this value when you need to determine when new links are created.


#### Examples

The following code sample demonstrates how to create a new DFS link using a call to the 
    <b>NetDfsAdd</b> function. Because the sample specifies the value 
    <b>DFS_ADD_VOLUME</b> in the <i>Flags</i> parameter, the call to 
    <b>NetDfsAdd</b> fails if the DFS link already exists. To add additional targets to an 
    existing DFS link, you can specify zero in the <i>Flags</i> parameter.


```cpp
#include <windows.h>
#include <lm.h>
#include <lmdfs.h>
#include <stdio.h>
#pragma comment(lib, "NetApi32.lib")

void wmain(int argc, wchar_t *argv[ ])
{
   DWORD res;
   LPTSTR lpszComment;
   lpszComment = argc < 5 ? NULL : argv[4];
   //
   // Check for required parameters.
   //
   if (argc < 4)
      wprintf(L"Syntax: %s DfsEntryPath ServerName ShareName [\"Comment\"]\n", argv[0]);
   else
   {
      //
      // Call the NetDfsAdd function; fail the call 
      // if the DFS link already exists (DFS_ADD_VOLUME).
         //
      // To add a second storage to a DFS link, change
      // the last parameter to 0.
      //
      res = NetDfsAdd(argv[1], argv[2], argv[3], lpszComment, DFS_ADD_VOLUME);
      //
      // If the call succeeds,
      //
      if(res == 0)
         printf("Added DFS link\n");
      else
         printf("Error: %u\n", res);
   }
   return;
}

```

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System 
    (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot">NetDfsAddFtRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot">NetDfsAddStdRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove">NetDfsRemove</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>