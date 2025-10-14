---
UID: NS:lmshare._SHARE_INFO_1005
title: SHARE_INFO_1005 (lmshare.h)
description: Contains information about the shared resource.
helpviewer_keywords: ["*LPSHARE_INFO_1005","*PSHARE_INFO_1005","CSC_MASK","CSC_MASK_EXT","LPSHARE_INFO_1005","LPSHARE_INFO_1005 structure pointer [Files]","PSHARE_INFO_1005","PSHARE_INFO_1005 structure pointer [Files]","SHARE_INFO_1005","SHARE_INFO_1005 structure [Files]","SHI1005_FLAGS_ACCESS_BASED_DIRECTORY_ENUM","SHI1005_FLAGS_ALLOW_NAMESPACE_CACHING","SHI1005_FLAGS_DFS","SHI1005_FLAGS_DFS_ROOT","SHI1005_FLAGS_ENABLE_CA","SHI1005_FLAGS_ENABLE_HASH","SHI1005_FLAGS_FORCE_LEVELII_OPLOCK","SHI1005_FLAGS_FORCE_SHARED_DELETE","SHI1005_FLAGS_RESTRICT_EXCLUSIVE_OPENS","_win32_share_info_1005_str","fs.share_info_1005_str","lmshare/LPSHARE_INFO_1005","lmshare/PSHARE_INFO_1005","lmshare/SHARE_INFO_1005","netmgmt.share_info_1005_str"]
old-location: fs\share_info_1005_str.htm
tech.root: fs
ms.assetid: 9fb3e0ae-76b5-4432-80dd-f3361738aa7c
ms.date: 12/05/2018
ms.keywords: '*LPSHARE_INFO_1005, *PSHARE_INFO_1005, CSC_MASK, CSC_MASK_EXT, LPSHARE_INFO_1005, LPSHARE_INFO_1005 structure pointer [Files], PSHARE_INFO_1005, PSHARE_INFO_1005 structure pointer [Files], SHARE_INFO_1005, SHARE_INFO_1005 structure [Files], SHI1005_FLAGS_ACCESS_BASED_DIRECTORY_ENUM, SHI1005_FLAGS_ALLOW_NAMESPACE_CACHING, SHI1005_FLAGS_DFS, SHI1005_FLAGS_DFS_ROOT, SHI1005_FLAGS_ENABLE_CA, SHI1005_FLAGS_ENABLE_HASH, SHI1005_FLAGS_FORCE_LEVELII_OPLOCK, SHI1005_FLAGS_FORCE_SHARED_DELETE, SHI1005_FLAGS_RESTRICT_EXCLUSIVE_OPENS, _win32_share_info_1005_str, fs.share_info_1005_str, lmshare/LPSHARE_INFO_1005, lmshare/PSHARE_INFO_1005, lmshare/SHARE_INFO_1005, netmgmt.share_info_1005_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHARE_INFO_1005, *PSHARE_INFO_1005, *LPSHARE_INFO_1005
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHARE_INFO_1005
 - lmshare/_SHARE_INFO_1005
 - PSHARE_INFO_1005
 - lmshare/PSHARE_INFO_1005
 - SHARE_INFO_1005
 - lmshare/SHARE_INFO_1005
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmshare.h
api_name:
 - SHARE_INFO_1005
---

# SHARE_INFO_1005 structure


## -description

Contains information about the shared resource.

## -struct-fields

### -field shi1005_flags

A bitmask of flags that specify information about the shared resource.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_DFS"></a><a id="shi1005_flags_dfs"></a><dl>
<dt><b>SHI1005_FLAGS_DFS</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The specified share is present in a Dfs tree structure. This flag cannot be set with 
        <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_DFS_ROOT"></a><a id="shi1005_flags_dfs_root"></a><dl>
<dt><b>SHI1005_FLAGS_DFS_ROOT</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The specified share is the root volume in a Dfs tree structure. This flag cannot be set with 
        <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_RESTRICT_EXCLUSIVE_OPENS"></a><a id="shi1005_flags_restrict_exclusive_opens"></a><dl>
<dt><b>SHI1005_FLAGS_RESTRICT_EXCLUSIVE_OPENS</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The specified share disallows exclusive file opens, where reads to an open file are disallowed.

</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_FORCE_SHARED_DELETE"></a><a id="shi1005_flags_force_shared_delete"></a><dl>
<dt><b>SHI1005_FLAGS_FORCE_SHARED_DELETE</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Shared files in the specified share can be forcibly deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_ALLOW_NAMESPACE_CACHING"></a><a id="shi1005_flags_allow_namespace_caching"></a><dl>
<dt><b>SHI1005_FLAGS_ALLOW_NAMESPACE_CACHING</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Clients are allowed to cache the namespace of the specified share.

</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_ACCESS_BASED_DIRECTORY_ENUM"></a><a id="shi1005_flags_access_based_directory_enum"></a><dl>
<dt><b>SHI1005_FLAGS_ACCESS_BASED_DIRECTORY_ENUM</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
The server will filter directory entries based on the access permissions that the user on the  client computer has for the server on which the files reside. 
        Only files for which the user has read access and directories for which the user has FILE_LIST_DIRECTORY access will be returned. If the user has SeBackupPrivilege, all available information will be returned.

For more information about file and directory access, see <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

For more information about SeBackupPrivilege, see <a href="/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>.

<div class="alert"><b>Note</b>  This flag is supported only on servers running Windows Server 2003 with SP1 or later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_FORCE_LEVELII_OPLOCK"></a><a id="shi1005_flags_force_levelii_oplock"></a><dl>
<dt><b>SHI1005_FLAGS_FORCE_LEVELII_OPLOCK</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Prevents exclusive caching modes that can cause delays for highly shared read-only data. 

<div class="alert"><b>Note</b>  This flag is supported only on servers running Windows Server 2008 R2 or later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_ENABLE_HASH"></a><a id="shi1005_flags_enable_hash"></a><dl>
<dt><b>SHI1005_FLAGS_ENABLE_HASH</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Enables server-side functionality needed for peer caching support. Clients on high-latency or low-bandwidth connections can use alternate methods to retrieve data from peers if available, instead of sending requests to the server. This is only supported on shares configured for manual caching (CSC_CACHE_MANUAL_REINT).

<div class="alert"><b>Note</b>  This flag is supported only on servers running Windows Server 2008 R2 or later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="SHI1005_FLAGS_ENABLE_CA"></a><a id="shi1005_flags_enable_ca"></a><dl>
<dt><b>SHI1005_FLAGS_ENABLE_CA</b></dt>
<dt>0X4000</dt>
</dl>
</td>
<td width="60%">
Enables Continuous Availability on a cluster share. Handles that are opened against a continuously available share can survive network failures as well as cluster node failures.

<div class="alert"><b>Note</b>  This flag can only be set on a scoped share on a server that meets the following conditions:<ul>
<li>It is running Windows Server 2012 or later. </li>
<li>It is in a cluster configuration.</li>
<li>It has  the "Services for Continuously Available shares" role service installed.</li>
</ul>
</div>
<div> </div>
<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008 and Windows Server 2003:  </b>This flag is not supported.

</td>
</tr>
</table>
 

The CSC_MASK and CSC_MASK_EXT mask values can be used to apply flags that are specific to client-side caching (CSC).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CSC_MASK"></a><a id="csc_mask"></a><dl>
<dt><b>CSC_MASK</b></dt>
<dt>0x0030</dt>
</dl>
</td>
<td width="60%">
Provides a mask for the following CSC states.

<dl>
<dt><b>CSC_CACHE_MANUAL_REINT</b> 0x0000</dt>
<dd>
Automatic file-by-file reintegration is not allowed.

</dd>
<dt><b>CSC_CACHE_AUTO_REINT</b> 0x0010</dt>
<dd>
File-by-file reintegration is allowed.

</dd>
<dt><b>CSC_CACHE_VDO</b> 0x0020</dt>
<dd>
File opens do not need to be flowed.

</dd>
<dt><b>CSC_CACHE_NONE</b> 0x0030</dt>
<dd>
CSC is disabled for this share.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="CSC_MASK_EXT"></a><a id="csc_mask_ext"></a><dl>
<dt><b>CSC_MASK_EXT</b></dt>
<dt>0x2030</dt>
</dl>
</td>
<td width="60%">
Provides a mask for the following CSC states and options.

<dl>
<dt><b>CSC_CACHE_MANUAL_REINT</b> 0x0000</dt>
<dd>
Automatic file-by-file reintegration is not allowed.

</dd>
<dt><b>CSC_CACHE_AUTO_REINT</b> 0x0010</dt>
<dd>
File-by-file reintegration is allowed.

</dd>
<dt><b>CSC_CACHE_VDO</b> 0x0020</dt>
<dd>
File opens do not need to be flowed.

</dd>
<dt><b>CSC_CACHE_NONE</b> 0x0030</dt>
<dd>
CSC is disabled for this share.

</dd>
<dt><b>SHI1005_FLAGS_ENABLE_HASH</b> 0x2000</dt>
<dd>
Enables server-side functionality needed for peer caching support.

</dd>
</dl>
</td>
</tr>
</table>

## -remarks

This structure can be retrieved by calling the 
    <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> function. It can be set by calling the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a> function.

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo">NetShareSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>