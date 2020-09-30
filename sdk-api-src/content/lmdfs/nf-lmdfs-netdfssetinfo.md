---
UID: NF:lmdfs.NetDfsSetInfo
title: NetDfsSetInfo function (lmdfs.h)
description: Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.
helpviewer_keywords: ["100","101","102","103","104","105","106","107","150","NetDfsSetInfo","NetDfsSetInfo function [Distributed File System]","_win32_netdfssetinfo","dfs.netdfssetinfo","fs.netdfssetinfo","lmdfs/NetDfsSetInfo","netmgmt.netdfssetinfo"]
old-location: dfs\netdfssetinfo.htm
tech.root: Dfs
ms.assetid: 5526afa7-82bc-47c7-99d6-44e41ef772b1
ms.date: 12/05/2018
ms.keywords: 100, 101, 102, 103, 104, 105, 106, 107, 150, NetDfsSetInfo, NetDfsSetInfo function [Distributed File System], _win32_netdfssetinfo, dfs.netdfssetinfo, fs.netdfssetinfo, lmdfs/NetDfsSetInfo, netmgmt.netdfssetinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetDfsSetInfo
 - lmdfs/NetDfsSetInfo
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
 - NetDfsSetInfo
---

# NetDfsSetInfo function


## -description

Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link 
    target.

## -parameters

### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>&#92;<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>&#92;<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace; <i>DomDfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i>  is a DFS link.

For a root, the string can be in one of two forms:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

or

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>

where the values of the names are the same as those described previously.

### -param ServerName [in, optional]

Pointer to a string that specifies the DFS link target server name. This parameter is optional. For more 
      information, see the Remarks section.

### -param ShareName [in, optional]

Pointer to a string that specifies the DFS link target share name. This may also be a share name with a 
      path relative to the share.  For example, "share1\mydir1\mydir2". This parameter is optional. For more 
      information, see the Remarks section.

### -param Level [in]

Specifies the information level of the data. This parameter can be one of the following values.



#### 100

Set the comment associated with the DFS root or link specified in the 
        <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100">DFS_INFO_100</a> structure.



#### 101

Set the storage state associated with the DFS root or link specified in the 
        <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101">DFS_INFO_101</a> structure.



#### 102

Set the time-out value associated with the DFS root or link specified in the 
        <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
        <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102">DFS_INFO_102</a> structure.



#### 103

Set the property flags for the DFS root or link specified in the <i>DfsEntryPath</i> 
         parameter. The <i>Buffer</i> parameter points to a 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103">DFS_INFO_103</a> structure.



#### 104

Set the target priority rank and class for the root target or link target specified in the 
         <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104">DFS_INFO_104</a> structure.



#### 105

Set the comment, state, and time-out information, as well as property flags, for the DFS root or link 
         specified in the <i>DfsEntryPath</i> parameter. The <i>Buffer</i> 
         parameter points to a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105">DFS_INFO_105</a> structure.



#### 106

Set the target state and priority for the root target or link target specified in the 
         <i>DfsEntryPath</i> parameter. This information cannot be set for a DFS namespace root or 
         link, only for a root target or link target. The <i>Buffer</i> parameter points to a 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106">DFS_INFO_106</a> structure.



#### 107

Set the comment, state, time-out information, and property flags for the DFS root or link specified in the 
         <i>DfsEntryPath</i> parameter. For DFS links, you can also set the security descriptor for 
         the link's reparse point. The <i>Buffer</i> parameter points to a 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107">DFS_INFO_107</a> structure.



#### 150

Set the security descriptor for a DFS link's reparse point. The <i>Buffer</i> parameter 
         points to a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150">DFS_INFO_150</a> structure.

### -param Buffer [in]

Pointer to a buffer that specifies the data. The format of this data depends on the value of the 
      <i>Level</i> parameter. For more information, see 
      <a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The caller must have Administrator privilege on the DFS server. For more information about calling functions 
    that require administrator privileges, see 
    <a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

If you specify both the <i>ServerName</i> and <i>ShareName</i> 
    parameters, the <b>NetDfsSetInfo</b> function sets or modifies information specific to 
    that root target or link target. If the parameters are <b>NULL</b>, the function sets or 
    modifies information that is specific to the DFS namespace root or the DFS link instead of a specific DFS root 
    target or link target.

Because only one comment and one time-out can be set for a DFS root or link, the 
    <i>ServerName</i> and <i>ShareName</i>  parameters are ignored for 
    information levels 100 and 102. These parameters are required for level 101.

For information level 101, the <b>DFS_VOLUME_STATE_RESYNCHRONIZE</b> and <b>DFS_VOLUME_STATE_STANDBY</b> state values can be 
     set as follows for a specific domain-based DFS root when there is more than one DFS root target for the DFS 
     namespace:

The <i>DfsEntryPath</i> parameter specifies the domain-based DFS namespace, and the 
      <i>ServerName</i> and <i>ShareName</i> parameters taken together specify 
      the DFS root target on which the set-information operation is to be performed.


#### Examples

The following code sample demonstrates how to associate a comment with a DFS link using a call to the 
     <b>NetDfsSetInfo</b> function. The sample specifies information level 100 
     (<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100">DFS_INFO_100</a>).


```cpp
#include <windows.h>
#include <lm.h>
#include <lmdfs.h>
#include <stdio.h>
#pragma comment(lib, "Netapi32.lib")

void wmain(int argc, wchar_t *argv[])
{
   DFS_INFO_100 dfsData;
   DWORD res;
   //
   // Check command line arguments.
   //
   if (argc<2)
      wprintf(L"Syntax: %s DfsEntryPath [\"Comment\"]\n", argv[0]);
   else
   {
      //
      // Fill in DFS_INFO_100 structure member.
      //
      dfsData.Comment = argc < 3 ? NULL : argv[2];
      //
      // Call the NetDfsSetInfo function, specifying level 100.
      //
      res = NetDfsSetInfo(argv[1], NULL, NULL, 100, (LPBYTE) &dfsData);
      //
      // Display the result of the call.
      //
      if(res == 0)
         printf("Comment set.\n");
      else
         printf("Error: %u", res);
   }
   return;
}

```

## -see-also

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100">DFS_INFO_100</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101">DFS_INFO_101</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102">DFS_INFO_102</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103">DFS_INFO_103</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104">DFS_INFO_104</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105">DFS_INFO_105</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106">DFS_INFO_106</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107">DFS_INFO_107</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150">DFS_INFO_150</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>