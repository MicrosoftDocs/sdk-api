---
UID: NS:lmdfs._DFS_INFO_107
title: DFS_INFO_107 (lmdfs.h)
description: Contains information about a DFS root or link, including the comment, state, time-out, property flags, and link reparse point security descriptor.
helpviewer_keywords: ["*LPDFS_INFO_107","*PDFS_INFO_107","DFS_INFO_107","DFS_INFO_107 structure [Distributed File System]","DFS_PROPERTY_FLAG_ABDE","DFS_PROPERTY_FLAG_CLUSTER_ENABLED","DFS_PROPERTY_FLAG_INSITE_REFERRALS","DFS_PROPERTY_FLAG_ROOT_SCALABILITY","DFS_PROPERTY_FLAG_SITE_COSTING","DFS_PROPERTY_FLAG_TARGET_FAILBACK","DFS_VOLUME_FLAVOR_AD_BLOB","DFS_VOLUME_FLAVOR_STANDALONE","DFS_VOLUME_STATE_INCONSISTENT","DFS_VOLUME_STATE_OFFLINE","DFS_VOLUME_STATE_OK","DFS_VOLUME_STATE_ONLINE","PDFS_INFO_107","PDFS_INFO_107 structure pointer [Distributed File System]","dfs.dfs_info_107","fs.dfs_info_107","lmdfs/DFS_INFO_107","lmdfs/PDFS_INFO_107"]
old-location: dfs\dfs_info_107.htm
tech.root: Dfs
ms.assetid: 38afc682-bb37-42ad-9e92-a1b0aa277f29
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_107, *PDFS_INFO_107, DFS_INFO_107, DFS_INFO_107 structure [Distributed File System], DFS_PROPERTY_FLAG_ABDE, DFS_PROPERTY_FLAG_CLUSTER_ENABLED, DFS_PROPERTY_FLAG_INSITE_REFERRALS, DFS_PROPERTY_FLAG_ROOT_SCALABILITY, DFS_PROPERTY_FLAG_SITE_COSTING, DFS_PROPERTY_FLAG_TARGET_FAILBACK, DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, PDFS_INFO_107, PDFS_INFO_107 structure pointer [Distributed File System], dfs.dfs_info_107, fs.dfs_info_107, lmdfs/DFS_INFO_107, lmdfs/PDFS_INFO_107'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DFS_INFO_107, *PDFS_INFO_107, *LPDFS_INFO_107
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_INFO_107
 - lmdfs/_DFS_INFO_107
 - PDFS_INFO_107
 - lmdfs/PDFS_INFO_107
 - DFS_INFO_107
 - lmdfs/DFS_INFO_107
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
 - DFS_INFO_107
---

# DFS_INFO_107 structure


## -description

Contains information about a DFS root or link, including the comment, state, time-out, property flags, 
     and link reparse point security descriptor. This structure is only for use with the 
     <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> and 
     <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a> functions.

## -struct-fields

### -field Comment

Pointer to a null-terminated Unicode string that contains a comment associated with the DFS root or 
      link.

### -field State

Specifies a set of bit flags that describe the DFS root or link. One 
      <b>DFS_VOLUME_STATE</b> flag is set, and one <b>DFS_VOLUME_FLAVOR</b> flag 
      is set. The <b>DFS_VOLUME_FLAVORS</b> bitmask (0x00000300) must be used to extract the DFS 
      namespace flavor, and the <b>DFS_VOLUME_STATES</b> bitmask (0x0000000F) must be used to 
      extract the DFS root or link state from this member. For an example that describes the interpretation of the 
      flags, see the Remarks section of <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a>.



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

### -field PropertyFlagMask

Specifies a mask value that indicates which flags are valid for evaluation in the 
      <b>PropertyFlags</b> field.

### -field PropertyFlags

Bitfield, with each bit responsible for a specific property applicable to the whole DFS namespace, the DFS 
      root, or an individual DFS link, depending on the actual property.  Any combination of bits is allowed unless 
      indicated otherwise.



#### DFS_PROPERTY_FLAG_INSITE_REFERRALS (0x00000001)

Referral response from a DFS server for a DFS root or link that contains only those targets in the same 
         site as the client requesting the referral. Targets in the two global priority classes are always returned, 
         regardless of their site location. This flag applies to domain-based DFS roots, stand-alone DFS roots, and 
         DFS links. If this flag is set at the DFS root, it applies to all links; otherwise, it applies to an 
         individual link. The setting at the link does not override the root setting.



#### DFS_PROPERTY_FLAG_ROOT_SCALABILITY (0x00000002)

If this flag is set, the DFS server polls the nearest domain controller (DC) instead of the primary domain 
         controller (PDC) to check for DFS namespace changes for that namespace. Any modification to the DFS metadata 
         by the DFS server is not controlled by this flag but is sent to the PDC. This flag is valid for the entire 
         namespace and applies only to domain-based DFS namespaces.



#### DFS_PROPERTY_FLAG_SITE_COSTING (0x00000004)

Set this flag to enable Active Directory site costing of targets. Targets returned from the DFS server to 
         the requesting DFS client are grouped by inter-site cost with respect to the DFS client. The groups are 
         ordered in terms of increasing site cost with the first group consisting of targets in the same site as the 
         client. Targets within each group are ordered randomly.

If this flag is not enabled, the default return is two sets: one set of targets in the same site as the 
         client, and one set of all remaining targets. This flag is valid for the entire DFS namespace and applies to 
         both domain-based and stand-alone DFS namespaces.

Target priorities can further influence target ordering. For more information on how site-costing is used 
         to prioritize targets, see 
         <a href="/previous-versions/windows/desktop/dfs/dfs-server-target-prioritization">DFS Server Target Prioritization</a>.



#### DFS_PROPERTY_FLAG_TARGET_FAILBACK (0x00000008)

Set this flag to enable V4 DFS clients to fail back to a more optimal (lower cost or higher priority) 
         target. If this flag is set at the DFS root, it applies to all links; otherwise, it applies to an individual 
         link. An individual link setting will not override a root setting. The target failback setting is provided to 
         the DFS client in a V4 referral response by the DFS server. This flag applies to domain-based roots, 
         stand-alone roots, and links.



#### DFS_PROPERTY_FLAG_CLUSTER_ENABLED (0x00000010)

If this flag is set, the DFS root is clustered to provide high availability for storage failover. This 
        flag cannot be set using the <a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a> function 
        and applies only to stand-alone DFS roots and links.



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

### -field SecurityDescriptorLength

### -field pSecurityDescriptor.size_is

### -field pSecurityDescriptor.size_is.SecurityDescriptorLength

### -field SdLengthReserved

This member is reserved for system use.

### -field pSecurityDescriptor

Pointer to a  <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> 
      structure that specifies a self-relative security descriptor to be associated with the DFS link's reparse point. 
      This field is valid for DFS links only.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a>