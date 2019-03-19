---
UID: NS:lmdfs._DFS_INFO_5
title: DFS_INFO_5 (lmdfs.h)
author: windows-sdk-content
description: Contains information about a Distributed File System (DFS) root or link. This structure contains the name, status, GUID, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.
old-location: dfs\dfs_info_5.htm
tech.root: Dfs
ms.assetid: bd68d7bf-94e1-41f9-84e9-e58ab34378a1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDFS_INFO_5, *PDFS_INFO_5, DFS_INFO_5, DFS_INFO_5 structure [Distributed File System], DFS_PROPERTY_FLAG_ABDE, DFS_PROPERTY_FLAG_CLUSTER_ENABLED, DFS_PROPERTY_FLAG_INSITE_REFERRALS, DFS_PROPERTY_FLAG_ROOT_SCALABILITY, DFS_PROPERTY_FLAG_SITE_COSTING, DFS_PROPERTY_FLAG_TARGET_FAILBACK, DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, LPDFS_INFO_5, LPDFS_INFO_5 structure pointer [Distributed File System], PDFS_INFO_5, PDFS_INFO_5 structure pointer [Distributed File System], dfs.dfs_info_5, fs.dfs_info_5, lmdfs/DFS_INFO_5, lmdfs/LPDFS_INFO_5, lmdfs/PDFS_INFO_5, netmgmt.dfs_info_5"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_5
product: Windows
targetos: Windows
req.typenames: DFS_INFO_5, *PDFS_INFO_5, *LPDFS_INFO_5
req.redist: 
---

# DFS_INFO_5 structure


## -description


Contains information about a Distributed File System (DFS) root or link. This structure contains the 
    name, status, <b>GUID</b>, time-out, namespace/root/link properties, metadata size, and number of targets for the root or 
    link. This structure is only for use with the <a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>, 
    <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>, and 
    <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> functions.

To retrieve information about the targets of the DFS namespace, use 
    <a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a> instead.


## -struct-fields




### -field EntryPath

Pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) path 
       of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

\\<i>ServerName</i>\<i>DfsName</i>\<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

\\<i>DomainName</i>\<i>DomDfsname</i>\<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace; <i>DomDfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

\\<i>ServerName</i>\<i>DfsName</i>

or

\\<i>DomainName</i>\<i>DomDfsname</i>

where the values of the names are the same as those described previously.


### -field Comment

Pointer to a null-terminated Unicode string that contains a comment associated with the DFS root or 
      link.


### -field State

Specifies a set of bit flags that describe the DFS root or link. One 
      <b>DFS_VOLUME_STATE</b> flag is set, and one <b>DFS_VOLUME_FLAVOR</b> flag 
      is set. For an example that describes the interpretation of the flags, see the Remarks section of 
      <a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a>.



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
        <a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a> function.



#### DFS_PROPERTY_FLAG_ABDE (0x00000020)

Scope: Domain-based DFS roots and stand-alone DFS roots.

When this flag is set, Access-Based Directory Enumeration (ABDE) mode support is enabled on the entire DFS 
         root target share of the DFS namespace. This flag is valid only for DFS namespaces for which the 
         <b>DFS_NAMESPACE_CAPABILITY_ABDE</b> capability flag is set. For more information, see 
         <a href="https://msdn.microsoft.com/1af2866c-fe83-43fc-b4cc-9976157fb269">DFS_INFO_50</a> and 
         <a href="https://msdn.microsoft.com/ee75c500-70c6-4dce-9d38-36cacd695746">DFS_SUPPORTED_NAMESPACE_VERSION_INFO</a>.

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
     <a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a> structure. 
     <b>DFS_INFO_5</b> is used to specify information about a DFS 
     namespace without target information.




## -see-also




<a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

