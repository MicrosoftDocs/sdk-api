---
UID: NF:lmdfs.NetDfsAddRootTarget
title: NetDfsAddRootTarget function (lmdfs.h)
description: Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.
helpviewer_keywords: ["NetDfsAddRootTarget","NetDfsAddRootTarget function [Distributed File System]","dfs.netdfsaddroottarget","fs.netdfsaddroottarget","lmdfs/NetDfsAddRootTarget"]
old-location: dfs\netdfsaddroottarget.htm
tech.root: Dfs
ms.assetid: c4ce8f50-f090-4783-b6c9-834d9e0c33de
ms.date: 12/05/2018
ms.keywords: NetDfsAddRootTarget, NetDfsAddRootTarget function [Distributed File System], dfs.netdfsaddroottarget, fs.netdfsaddroottarget, lmdfs/NetDfsAddRootTarget
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
 - NetDfsAddRootTarget
 - lmdfs/NetDfsAddRootTarget
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
 - NetDfsAddRootTarget
---

# NetDfsAddRootTarget function


## -description

Creates a domain-based or stand-alone  DFS namespace or adds a new root target to an existing domain-based namespace.

## -parameters

### -param pDfsPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS namespace.

For a stand-alone DFS namespace, this string should be in the following format:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

where <i>ServerName</i> is the name of the server that will host the new DFS root target and <i>DfsName</i> is the name of the DFS namespace.

For a domain-based DFS namespace, this string should be in the following format:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsName</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS namespace and <i>DomDfsName</i> is the name of the new or existing domain-based DFS namespace. For compatibility reasons, <i>DomDfsName</i> should be the same as the name of the shared folder on the server that will host the new DFS root target.

### -param pTargetPath [in, optional]

Pointer to a null-terminated Unicode string that specifies the UNC path of a DFS root target for the DFS namespace that is specified in the <i>pDfsPath</i> parameter.

For a stand-alone DFS namespace, this parameter must be <b>NULL</b>. For a domain-based DFS namespace, the string should be in the following format:

&#92;&#92;<i>ServerName</i>&#92;<i>RootShare</i>

where <i>ServerName</i> is the name of the server that will host the new DFS root target and <i>RootShare</i> is the name of the shared folder on the server. The share specified by <i>RootShare</i> must already exist on the server that will host the new DFS root target. This function does not create a new share.

### -param MajorVersion [in]

Specifies the DFS metadata version for the namespace.

<div class="alert"><b>Note</b>  This parameter is only for use when creating a new namespace.</div>
<div> </div>
If a stand-alone DFS namespace is being created, this parameter must be set to 1.

If a domain-based namespace is being created, this parameter should be set as follows:

<ul>
<li>Set it to 1 to specify Windows 2000 mode.</li>
<li>Set it to 2 or higher to specify  Windows Server 2008 mode.</li>
</ul>
If a new root target is being added to an existing domain-based DFS namespace, this parameter must be set to zero.

### -param pComment [in, optional]

Pointer to a null-terminated Unicode string that contains a comment associated with the DFS root.

### -param Flags [in]

This parameter is reserved and must be zero.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the domain is not at the required functional level for the specified <i>MajorVersion</i>, the return value is <b>ERROR_DS_INCOMPATIBLE</b>. This return value applies only to domain roots and a <i>MajorVersion</i> of 2.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The caller must have Administrator privilege on the DFS server.

To determine the DFS metadata version that can be specified in the <i>MajorVersion</i> parameter, use the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion">NetDfsGetSupportedNamespaceVersion</a> function.

The following table shows which parameter values you should specify, according to the desired result.

<table>
<tr>
<th><i>pDfsPath</i> parameter</th>
<th><i>pTargetPath</i> parameter</th>
<th><i>MajorVersion</i> parameter</th>
<th>Result</th>
</tr>
<tr>
<td>&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsName</i></td>
<td>&#92;&#92;<i>ServerName</i>&#92;<i>RootShare</i></td>
<td>
1

</td>
<td>
Create a Windows 2000 mode domain-based DFS namespace or add a new root target to an existing one.

</td>
</tr>
<tr>
<td>&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsName</i></td>
<td>&#92;&#92;<i>ServerName</i>&#92;<i>RootShare</i></td>
<td>
2

</td>
<td>
Create a  Windows Server 2008 mode domain-based DFS namespace or add a new root target to an existing one.

</td>
</tr>
<tr>
<td>&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsName</i></td>
<td>&#92;&#92;<i>ServerName</i>&#92;<i>RootShare</i></td>
<td>
0

</td>
<td>
Add a new root target to an existing Windows 2000 mode or Windows Server 2008 mode domain-based DFS namespace.

</td>
</tr>
<tr>
<td>&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i></td>
<td><b>NULL</b></td>
<td>
Must be 1.

</td>
<td>
Create a stand-alone DFS namespace.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/lmdfs/ne-lmdfs-dfs_namespace_version_origin">DFS_NAMESPACE_VERSION_ORIGIN</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System  (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot">NetDfsAddFtRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot">NetDfsAddStdRoot</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion">NetDfsGetSupportedNamespaceVersion</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget">NetDfsRemoveRootTarget</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>