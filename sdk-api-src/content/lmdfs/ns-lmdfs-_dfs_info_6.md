---
UID: NS:lmdfs._DFS_INFO_6
title: "_DFS_INFO_6"
author: windows-sdk-content
description: Contains information about a Distributed File System (DFS) root or link. This structure contains the name, status, GUID, time-out, namespace/root/link properties, metadata size, number of targets, and information about each target of the root or link.
old-location: dfs\dfs_info_6.htm
tech.root: Dfs
ms.assetid: 96a9c5eb-f79f-4577-b320-ebacff84fcc4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPDFS_INFO_6, *PDFS_INFO_6, DFS_INFO_6, DFS_INFO_6 structure [Distributed File System], DFS_PROPERTY_FLAG_ABDE, DFS_PROPERTY_FLAG_CLUSTER_ENABLED, DFS_PROPERTY_FLAG_INSITE_REFERRALS, DFS_PROPERTY_FLAG_ROOT_SCALABILITY, DFS_PROPERTY_FLAG_SITE_COSTING, DFS_PROPERTY_FLAG_TARGET_FAILBACK, DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, LPDFS_INFO_6, LPDFS_INFO_6 structure pointer [Distributed File System], PDFS_INFO_6, PDFS_INFO_6 structure pointer [Distributed File System], _DFS_INFO_6, dfs.dfs_info_6, fs.dfs_info_6, lmdfs/DFS_INFO_6, lmdfs/LPDFS_INFO_6, lmdfs/PDFS_INFO_6, netmgmt.dfs_info_6"
ms.prod: windows
ms.technology: windows-sdk
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
 - DFS_INFO_6
product: Windows
targetos: Windows
req.typenames: DFS_INFO_6, *PDFS_INFO_6, *LPDFS_INFO_6
req.redist: 
---

# _DFS_INFO_6 structure


## -description


Contains information about a Distributed File System (DFS) root or link. This structure contains the 
    name, status, <b>GUID</b>, time-out, namespace/root/link properties, metadata size, number of targets, and information 
    about each target of the root or link. This structure is only for use with the 
    <a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>, 
    <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>, and 
    <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> functions.

To obtain information about the DFS namespace without target information, use 
    <a href="https://msdn.microsoft.com/bd68d7bf-94e1-41f9-84e9-e58ab34378a1">DFS_INFO_5</a> instead.


## -struct-fields




### -field EntryPath

Pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) path of a 
       DFS root or link.

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
      is set. The <b>DFS_VOLUME_FLAVORS</b> bitmask (0x00000300) must be used to extract the DFS 
      namespace flavor, and the <b>DFS_VOLUME_STATES</b> bitmask (0x0000000F) must be used to 
      extract the DFS root or link state from this member. For an example that describes the interpretation of the 
      flags, see the Remarks section of <a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a>.



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

Specifies the <b>GUID</b> of the DFS root or link.


### -field PropertyFlags

Specifies a set of flags describing specific properties of a DFS namespace, root, or link.



#### DFS_PROPERTY_FLAG_INSITE_REFERRALS (0x00000001)

Scope: Domain roots, stand-alone roots, and links. If this flag is set at the DFS root, it applies to all 
         links; otherwise, the value of this flag is considered for each individual link.

When this flag is set, a DFS referral response from a DFS server for a DFS root or link with the "INSITE" 
         option enabled contains only those targets which are in the same site as the DFS client requesting the 
         referral. Targets in the two global priority classes are always returned, regardless of their site 
         location.



#### DFS_PROPERTY_FLAG_ROOT_SCALABILITY (0x00000002)

Scope: The entire DFS namespace for a domain-based DFS namespace only.

By default, a DFS root target server polls the PDS to detect changes to the DFS metadata. To prevent heavy 
         server load on the PDC, root scalability can be enabled for the DFS namespace. Setting this flag will cause 
         the DFS server to poll the nearest domain controller instead of the PDC for DFS metadata changes for the 
         common namespace. Note that any changes made to the metadata must still occur on the PDC, however.



#### DFS_PROPERTY_FLAG_SITE_COSTING (0x00000004)

Scope: The entire DFS namespace for both domain-based and stand-alone DFS namespaces.

By default, targets returned in a referral response from a DFS server to a DFS client for a DFS root or 
         link consists of two groups: targets in the same site as the client, and targets outside the site.

If site-costing is enabled for the Active Directory, the response can have more than two groups, with each 
         group containing targets with the same site cost for the specific DFS client requesting the referral. The 
         groups are ordered by increasing site cost. For more information about how site-costing is used to prioritize 
         targets, see 
         <a href="https://msdn.microsoft.com/0aacebf7-49cc-4287-a5c4-0d25a416d227">DFS Server Target Prioritization</a>.



#### DFS_PROPERTY_FLAG_TARGET_FAILBACK (0x00000008)

Scope: Domain-based DFS roots, stand-alone DFS roots, and DFS links. If this flag is set at the DFS root, 
         it applies to all links; otherwise, the value of this flag is considered for each individual link.

When this flag is set, optimal target failback is enabled for V4 DFS clients, allowing them to fail back to 
         an optimal target after failing over to a non-optimal one. The target failback setting is provided to the DFS 
         client in a V4 referral response by a DFS server.



#### DFS_PROPERTY_FLAG_CLUSTER_ENABLED (0x00000010)

Scope: Stand-alone DFS roots and links only.

 The DFS root is clustered to provide high availability for 
         storage failover. This flag cannot be set using the 
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
       blob, in bytes. For stand-alone DFS namespaces, this field specifies the size of the metadata stored in the 
       registry, including the key names and value names as well as the specific data items associated with them.

This field is valid for DFS roots only.


### -field NumberOfStorages

Specifies the number of targets for the DFS root or link. These targets are contained in the 
      <b>Storage</b> member of this structure.


### -field Storage.size_is

 


### -field Storage.size_is.NumberOfStorages

 


### -field Storage

Specifies an array of <a href="https://msdn.microsoft.com/777b9688-9e34-48dd-bc8c-df17bef396d0">DFS_STORAGE_INFO_1</a> 
      structures that contain the DFS target information.


## -remarks



For more information about how server target priority is determined, see 
     <a href="https://msdn.microsoft.com/0aacebf7-49cc-4287-a5c4-0d25a416d227">DFS Server Target Prioritization</a>.




## -see-also




<a href="https://msdn.microsoft.com/0aacebf7-49cc-4287-a5c4-0d25a416d227">DFS Server Target Prioritization</a>



<a href="https://msdn.microsoft.com/777b9688-9e34-48dd-bc8c-df17bef396d0">DFS_STORAGE_INFO_1</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

