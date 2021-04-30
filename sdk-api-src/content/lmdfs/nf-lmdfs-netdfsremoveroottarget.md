---
UID: NF:lmdfs.NetDfsRemoveRootTarget
title: NetDfsRemoveRootTarget function (lmdfs.h)
description: Removes a DFS root target from a domain-based DFS namespace. If the root target is the last root target in the DFS namespace, this function removes the DFS namespace. This function can also be used to remove a stand-alone DFS namespace.
helpviewer_keywords: ["DFS_FORCE_REMOVE","NetDfsRemoveRootTarget","NetDfsRemoveRootTarget function [Distributed File System]","dfs.netdfsremoveroottarget","fs.netdfsremoveroottarget","lmdfs/NetDfsRemoveRootTarget"]
old-location: dfs\netdfsremoveroottarget.htm
tech.root: Dfs
ms.assetid: 9a8c78f4-3170-4568-940c-1c51aebad3ae
ms.date: 12/05/2018
ms.keywords: DFS_FORCE_REMOVE, NetDfsRemoveRootTarget, NetDfsRemoveRootTarget function [Distributed File System], dfs.netdfsremoveroottarget, fs.netdfsremoveroottarget, lmdfs/NetDfsRemoveRootTarget
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
 - NetDfsRemoveRootTarget
 - lmdfs/NetDfsRemoveRootTarget
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
 - NetDfsRemoveRootTarget
---

# NetDfsRemoveRootTarget function


## -description

Removes a DFS root target from a domain-based  DFS namespace. If the root target is the last root target 
    in the DFS namespace, this function removes the DFS namespace. This function can also be used to remove a 
    stand-alone DFS namespace.

## -parameters

### -param pDfsPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS namespace.

For a stand-alone DFS namespace, this string should be in the following form:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

where <i>ServerName</i> is the name of the server that hosts the DFS root target and 
       <i>DfsName</i> is the name of the DFS namespace.

For a domain-based DFS namespace, this string should be in the following form:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace and <i>DomDfsName</i> is the name of the DFS namespace.

### -param pTargetPath [in, optional]

Pointer to a null-terminated Unicode string that specifies the UNC path of a DFS root target for the DFS 
       namespace that is specified in the <i>pDfsPath</i> parameter.

For a stand-alone DFS namespace, this parameter must be <b>NULL</b>. For a domain-based 
       DFS namespace, the string should be in the following form:

&#92;&#92;<i>ServerName</i>&#92;<i>RootShare</i>

where <i>ServerName</i> is the name of the server that hosts the DFS root target and 
       <i>RootShare</i> is the name of the folder on the server.

### -param Flags [in]

A flag that specifies the type of removal operation. For a stand-alone DFS namespace, this parameter must 
      be zero. For a domain-based DFS namespace, it can be zero or the following value. If it is zero, this indicates 
      a normal removal operation.



#### DFS_FORCE_REMOVE (0x80000000)

If this flag is specified for a domain-based DFS namespace, the root target is removed even if it is not 
        accessible.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The caller must have Administrator privileges on the DFS server.

The following list shows which parameter values you should specify, according to the desired result.

<table>
<tr>
<th><i>pDfsPath</i> parameter</th>
<th><i>pTargetPath</i> parameter</th>
<th>Result</th>
</tr>
<tr>
<td>&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsName</i></td>
<td>&#92;&#92;<i>ServerName</i>&#92;<i>RootShare</i></td>
<td>Delete a Windows 2000 mode or Windows Server 2008 mode domain-based DFS root target. If the 
       target is the last root target for the DFS namespace, the function also deletes the DFS namespace.</td>
</tr>
<tr>
<td>&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i></td>
<td><b>NULL</b></td>
<td>Delete a stand-alone DFS namespace.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget">NetDfsAddRootTarget</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>