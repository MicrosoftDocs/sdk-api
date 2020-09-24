---
UID: NF:lmdfs.NetDfsGetSupportedNamespaceVersion
title: NetDfsGetSupportedNamespaceVersion function (lmdfs.h)
description: Determines the supported metadata version number.
helpviewer_keywords: ["NetDfsGetSupportedNamespaceVersion","NetDfsGetSupportedNamespaceVersion function [Distributed File System]","dfs.netdfsgetsupportednamespaceversion","fs.netdfsgetsupportednamespaceversion","lmdfs/NetDfsGetSupportedNamespaceVersion"]
old-location: dfs\netdfsgetsupportednamespaceversion.htm
tech.root: Dfs
ms.assetid: 32ccf4a7-9d07-45e1-93db-29eddee01680
ms.date: 12/05/2018
ms.keywords: NetDfsGetSupportedNamespaceVersion, NetDfsGetSupportedNamespaceVersion function [Distributed File System], dfs.netdfsgetsupportednamespaceversion, fs.netdfsgetsupportednamespaceversion, lmdfs/NetDfsGetSupportedNamespaceVersion
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
 - NetDfsGetSupportedNamespaceVersion
 - lmdfs/NetDfsGetSupportedNamespaceVersion
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
 - NetDfsGetSupportedNamespaceVersion
---

# NetDfsGetSupportedNamespaceVersion function


## -description

Determines the supported metadata version number.

## -parameters

### -param Origin [in]

A <a href="/previous-versions/windows/desktop/api/lmdfs/ne-lmdfs-dfs_namespace_version_origin">DFS_NAMESPACE_VERSION_ORIGIN</a> enumeration value that specifies the origin of the DFS namespace version.

### -param pName [in]

A string that specifies the server name or domain name. If the value of the <i>Origin</i> parameter is <b>DFS_NAMESPACE_VERSION_ORIGIN_DOMAIN</b>, this string must be an AD DS domain name. Otherwise, it must be a server name. This parameter is required and cannot be <b>NULL</b>.

### -param ppVersionInfo [out]

A pointer to a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a> structure that receives the DFS metadata version number.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function is useful in determining an appropriate version number to pass to the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget">NetDfsAddRootTarget</a> function.

The version number of the DFS metadata that can be used for a new DFS namespace depends on the following:

<ul>
<li>For domain-based DFS namespaces, the version supported by the DFS metadata schema that is being used in the AD DS domain.</li>
<li>The version supported by the server that is to host the DFS root target.</li>
</ul>
Thus, the maximum DFS metadata version number that can be used for a new DFS namespace is the minimum of the version supported by the AD DS domain and the version supported by the server. This maximum can be determined by calling the <b>NetDfsGetSupportedNamespaceVersion</b> function with the <i>pName</i> parameter set to the name of the server that is to host the new DFS root target and the <i>Origin</i> parameter set to <b>DFS_NAMESPACE_VERSION_ORIGIN_COMBINED</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/lmdfs/ne-lmdfs-dfs_namespace_version_origin">DFS_NAMESPACE_VERSION_ORIGIN</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget">NetDfsAddRootTarget</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
    Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
    Overview</a>