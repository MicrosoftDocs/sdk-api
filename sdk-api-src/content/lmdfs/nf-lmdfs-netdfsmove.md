---
UID: NF:lmdfs.NetDfsMove
title: NetDfsMove function (lmdfs.h)
description: Renames or moves a DFS link.
helpviewer_keywords: ["DFS_MOVE_FLAG_REPLACE_IF_EXISTS","NetDfsMove","NetDfsMove function [Distributed File System]","dfs.netdfsmove","fs.netdfsmove","lmdfs/NetDfsMove","netmgmt.netdfsmove"]
old-location: dfs\netdfsmove.htm
tech.root: Dfs
ms.assetid: d9d225ac-26b9-4074-93b6-6294538a3504
ms.date: 12/05/2018
ms.keywords: DFS_MOVE_FLAG_REPLACE_IF_EXISTS, NetDfsMove, NetDfsMove function [Distributed File System], dfs.netdfsmove, fs.netdfsmove, lmdfs/NetDfsMove, netmgmt.netdfsmove
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2008
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
 - NetDfsMove
 - lmdfs/NetDfsMove
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
 - NetDfsMove
---

# NetDfsMove function


## -description

Renames or moves a DFS link.

## -parameters

### -param OldDfsEntryPath [in]

Pointer to a string that specifies the source path for the move operation. This value must be a DFS link or 
     the path prefix of any DFS link in the DFS namespace.

### -param NewDfsEntryPath [in]

Pointer to a string that specifies the destination path for the move operation. This value must be a path or 
     a DFS link in the same DFS namespace.

### -param Flags [in]

A set of flags that describe actions to take when moving the link.



#### DFS_MOVE_FLAG_REPLACE_IF_EXISTS (0x00000001)

If the destination path is already an existing DFS link, replace it as part of the move operation.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The <b>NetDfsMove</b> function conveniently moves a link from an 
     old name to a new one. In the past, it has been necessary to perform the non-trivial action of deleting an 
     incorrect or old link and creating a new one, which becomes cumbersome when the link has a significant number of 
     targets or has per-target properties (like priority) set. It is also common for administrators to regularly 
     rename or move links.

DFS paths supplied to <b>NetDfsMove</b> can be either an actual 
     DFS link or just a DFS link path prefix. Wildcards are not allowed and only absolute paths can be specified. 
     Relative paths and special path name syntax (such as "." or "..") are not allowed.

When a DFS link path prefix is specified instead of a complete DFS path, the move operation is performed on all 
     DFS links which contain that prefix. Therefore, a single call to 
     <b>NetDfsMove</b> can "move" multiple links. However, the path 
     prefix must resolve to at least one valid DFS link or the move operation will fail.

The following examples demonstrate different move operations and the results.

<ol>
<li>
<ul>
<li>Old path: \\MyDfsServer\MyDfsShare\dir1\dir2\link1</li>
<li>New path: \\MyDfsServer\MyDfsShare\dir1\dir2\link2</li>
</ul>
After the move, \\MyDfsServer\MyDfsShare\dir1\dir2\link1 is replaced with 
       \\MyDfsServer\MyDfsShare\dir1\dir2\link2.

</li>
<li>
<ul>
<li>Old path: \\MyDfsServer\MyDfsShare\dir1\dir2\link1</li>
<li>New path: \\MyDfsServer\MyDfsShare\dir3\dir4\dir5\link2</li>
</ul>
After the move, \\MyDfsServer\MyDfsShare\dir1\dir2\link1 is replaced with 
       \\MyDfsServer\MyDfsShare\dir3\dir4\dir5\link2. Note that both the leaf and non-leaf components 
       have been renamed, and that the number of components in the new path has changed.

</li>
<li>
<ul>
<li>Old path: \\MyDfsServer\MyDfsShare\dir1</li>
<li>New path: \\MyDfsServer\MyDfsShare\dir3</li>
</ul>
After the move, all links prefixed with \\MyDfsServer\MyDfsShare\dir1 have that prefix replaced 
       with \\MyDfsServer\MyDfsShare\dir3. Therefore, 
       \\MyDfsServer\MyDfsShare\dir1\dir2\link1 and \\MyDfsServer\MyDfsShare\dir1\dir2\link2 
       are now \\MyDfsServer\MyDfsShare\dir3\dir2\link1 and 
       \\MyDfsServer\MyDfsShare\dir3\dir2\link1, respectively.

</li>
<li>
<ul>
<li>Old path: \\MyDfsServer\MyDfsShare\dir1</li>
<li>New path: \\MyDfsServer\MyDfsShare</li>
</ul>
After the move, all links prefixed with \\MyDfsServer\MyDfsShare\dir1 have that prefix replaced 
       with \\MyDfsServer\MyDfsShare. Therefore, \\MyDfsServer\MyDfsShare\dir1\dir2\link1 
       and \\MyDfsServer\MyDfsShare\dir1\dir2\link2 are now 
       \\MyDfsServer\MyDfsShare\dir2\link1 and \\MyDfsServer\MyDfsShare\dir2\link1, 
       respectively.

</li>
</ol>
If the new path already has an existing entry, <b>DFS_MOVE_FLAG_REPLACE_IF_EXISTS</b> must 
     be specified if the new path should overwrite the old one. When this flag is set, the collided path is deleted 
     and replaced by the new link. Note that any operation which can potentially result in DFS links that completely 
     overlap will fail, whether or not <b>DFS_MOVE_FLAG_REPLACE_IF_EXISTS</b> is specified. For 
     example:

<ul>
<li>Existing links: \\MyDfsServer\MyDfsShare\dir1\link1, 
      \\MyDfsServer\MyDfsShare\link3</li>
<li>Old path:\\MyDfsServer\MyDfsShare\dir1</li>
<li>New path: \\MyDfsServer\MyDfsShare\link3</li>
</ul>
If the move operation were allowed to succeed, the result would be two completely overlapping links: 
     \\MyDfsServer\MyDfsShare\link3\link1 and \\MyDfsServer\MyDfsShare\link3. Therefore, the 
     move operation must fail.

With domain-based DFS servers, the move operation is atomic; that is, either the whole operation is performed 
     or it fails. However, with stand-alone DFS servers, the move operation is not guaranteed to be atomic. In this 
     situation, a failure may result in a partially completed move operation and will require cleanup on behalf of the 
     calling application.

When the move operation succeeds, it is guaranteed that the DFS metadata was successfully modified. This does 
     not guarantee that the DFS links were actually created on the root targets or that DFS links can be created on 
     the root targets' storage.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>