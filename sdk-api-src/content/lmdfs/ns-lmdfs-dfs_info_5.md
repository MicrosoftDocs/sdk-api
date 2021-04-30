---
UID: NS:lmdfs._DFS_INFO_5
title: DFS_INFO_5 (lmdfs.h)
description: Contains information about a Distributed File System (DFS) root or link. This structure contains the name, status, GUID, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.
helpviewer_keywords: ["*LPDFS_INFO_5","*PDFS_INFO_5","DFS_INFO_5","DFS_INFO_5 structure [Distributed File System]","DFS_PROPERTY_FLAG_ABDE","DFS_PROPERTY_FLAG_CLUSTER_ENABLED","DFS_PROPERTY_FLAG_INSITE_REFERRALS","DFS_PROPERTY_FLAG_ROOT_SCALABILITY","DFS_PROPERTY_FLAG_SITE_COSTING","DFS_PROPERTY_FLAG_TARGET_FAILBACK","DFS_VOLUME_FLAVOR_AD_BLOB","DFS_VOLUME_FLAVOR_STANDALONE","DFS_VOLUME_STATE_INCONSISTENT","DFS_VOLUME_STATE_OFFLINE","DFS_VOLUME_STATE_OK","DFS_VOLUME_STATE_ONLINE","LPDFS_INFO_5","LPDFS_INFO_5 structure pointer [Distributed File System]","PDFS_INFO_5","PDFS_INFO_5 structure pointer [Distributed File System]","dfs.dfs_info_5","fs.dfs_info_5","lmdfs/DFS_INFO_5","lmdfs/LPDFS_INFO_5","lmdfs/PDFS_INFO_5","netmgmt.dfs_info_5"]
old-location: dfs\dfs_info_5.htm
tech.root: Dfs
ms.assetid: bd68d7bf-94e1-41f9-84e9-e58ab34378a1
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_5, *PDFS_INFO_5, DFS_INFO_5, DFS_INFO_5 structure [Distributed File System], DFS_PROPERTY_FLAG_ABDE, DFS_PROPERTY_FLAG_CLUSTER_ENABLED, DFS_PROPERTY_FLAG_INSITE_REFERRALS, DFS_PROPERTY_FLAG_ROOT_SCALABILITY, DFS_PROPERTY_FLAG_SITE_COSTING, DFS_PROPERTY_FLAG_TARGET_FAILBACK, DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, LPDFS_INFO_5, LPDFS_INFO_5 structure pointer [Distributed File System], PDFS_INFO_5, PDFS_INFO_5 structure pointer [Distributed File System], dfs.dfs_info_5, fs.dfs_info_5, lmdfs/DFS_INFO_5, lmdfs/LPDFS_INFO_5, lmdfs/PDFS_INFO_5, netmgmt.dfs_info_5'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DFS_INFO_5, *PDFS_INFO_5, *LPDFS_INFO_5
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_5
 - lmdfs/_DFS_INFO_5
 - PDFS_INFO_5
 - lmdfs/PDFS_INFO_5
 - DFS_INFO_5
 - lmdfs/DFS_INFO_5
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_5
---

# DFS_INFO_5 structure


## -description

Contains information about a Distributed File System (DFS) root or link. This structure contains the 
    name, status, <b>GUID</b>, time-out, namespace/root/link properties, metadata size, and number of targets for the root or 
    link. This structure is only for use with the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>, 
    <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>, and 
    <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> functions.

To retrieve information about the targets of the DFS namespace, use 
    <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6">DFS_INFO_6</a> instead.

## -struct-fields

### -field EntryPath

Pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) path 
       of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>&#92;<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>&#92;<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace; <i>DomDfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

&#92;&#92;<i>ServerName</i>&#92;<i>DfsName</i>

or

&#92;&#92;<i>DomainName</i>&#92;<i>DomDfsname</i>

where the values of the names are the same as those described previously.

### -field Comment

Pointer to a null-terminated Unicode string that contains a comment associated with the DFS root or 
      link.

### -field State

Specifies a set of bit flags that describe the DFS root or link. One 
      <b>DFS_VOLUME_STATE</b> flag is set, and one <b>DFS_VOLUME_FLAVOR</b> flag 
      is set. For an example that describes the interpretation of the flags, see the Remarks section of 
      <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a>.



#### DFS_VOLUME_STATE_OK (0x00000001)

The specified DFS root or link is in the normal state.



#### DFS_VOLUME_STATE_INCONSISTENT (0x00000002)

The internal DFS database is inconsistent with the specified DFS root or link. Attempts to repair the 
        inconsistency have failed.



#### DFS_VOLUME_STATE_OFFLINE (0x00000003)

The specified DFS root or link is offline or unavailable.



#### DFS_VOLUME_STATE_ONLINE (0x00000004)

The specified DFS root or link is available.



#### DFS_VOLUME_FLAVOR_STANDALONE (0x00000100)

The system sets this flag if the root is associated with a stand-alone DFS namespace.



#### DFS_VOLUME_FLAVOR_AD_BLOB (0x00000200)

The system sets this flag if the root is associated with a domain-based DFS namespace.

### -field Timeout

Specifies the time-out, in seconds, of the DFS root or link.

### -field Guid

Specifies the GUID of the DFS root or link.

### -field PropertyFlags

Specifies a set of flags describing specific properties of a DFS namespace, root, or link.



#### DFS_PROPERTY_FLAG_INSITE_REFERRALS (0x00000001)

Only targets in the same site as the client are returned. This flag is valid for both domain and 
        stand-alone roots and links.



#### DFS_PROPERTY_FLAG_ROOT_SCALABILITY (0x00000002)

The nearest domain controller is polled instead of the PDC for DFS namespace changes. This flag is only 
        valid for domain roots.



#### DFS_PROPERTY_FLAG_SITE_COSTING (0x00000004)

Active Directory site costing of targets is enabled, grouping targets into sets of increasing site costs 
        from DFS client to target. Each set has targets with the same cost. This flag is only valid for domain and 
        stand-alone roots.



#### DFS_PROPERTY_FLAG_TARGET_FAILBACK (0x00000008)

The DFS client fails back to a closer available target after failing over to a non-optimal target. This 
        flag is valid for both domain and stand-alone roots and links.



#### DFS_PROPERTY_FLAG_CLUSTER_ENABLED (0x00000010)

The DFS root is clustered. This flag cannot be set using the 
        <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a> function.



#### DFS_PROPERTY_FLAG_ABDE (0x00000020)

Scope: Domain-based DFS roots and stand-alone DFS roots.

When this flag is set, Access-Based Directory Enumeration (ABDE) mode support is enabled on the entire DFS 
         root target share of the DFS namespace. This flag is valid only for DFS namespaces for which the 
         <b>DFS_NAMESPACE_CAPABILITY_ABDE</b> capability flag is set. For more information, see 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50">DFS_INFO_50</a> and 
         <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>.

The <b>DFS_PROPERTY_FLAG_ABDE</b> flag is valid only on the DFS namespace root and not 
         on root targets, links, or link targets. This flag must be enabled to associate a security descriptor with a 
         DFS link.

### -field MetadataSize

For domain-based DFS namespaces, this member specifies the size of the corresponding Active Directory data 
       blob, in bytes. For stand-alone DFS namespaces, this member specifies the size of the metadata stored in the 
       registry, including the key names and value names as well as the specific data items associated with them.

This member is valid for DFS roots only.

### -field NumberOfStorages

Specifies the number of targets for the DFS root or link.

## -remarks

To retrieve information about targets and target priorities, use the 
     <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6">DFS_INFO_6</a> structure. 
     <b>DFS_INFO_5</b> is used to specify information about a DFS 
     namespace without target information.

## -see-also

<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6">DFS_INFO_6</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>