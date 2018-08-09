---
UID: NS:lmdfs._DFS_INFO_105
title: "_DFS_INFO_105"
author: windows-sdk-content
description: Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors specified by property flags.
old-location: dfs\dfs_info_105.htm
old-project: dfs
ms.assetid: b9ad9e41-d5b4-446f-ac99-a51808344f77
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDFS_INFO_105, *PDFS_INFO_105, DFS_INFO_105, DFS_INFO_105 structure [Distributed File System], DFS_PROPERTY_FLAG_ABDE, DFS_PROPERTY_FLAG_CLUSTER_ENABLED, DFS_PROPERTY_FLAG_INSITE_REFERRALS, DFS_PROPERTY_FLAG_ROOT_SCALABILITY, DFS_PROPERTY_FLAG_SITE_COSTING, DFS_PROPERTY_FLAG_TARGET_FAILBACK, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, Default, LPDFS_INFO_105, LPDFS_INFO_105 structure pointer [Distributed File System], PDFS_INFO_105, PDFS_INFO_105 structure pointer [Distributed File System], _DFS_INFO_105, dfs.dfs_info_105, fs.dfs_info_105, lmdfs/DFS_INFO_105, lmdfs/LPDFS_INFO_105, lmdfs/PDFS_INFO_105, netmgmt.dfs_info_105"
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
tech.root: 
req.typenames: DFS_INFO_105, *PDFS_INFO_105, *LPDFS_INFO_105
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_105
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_105 structure


## -description


Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors 
    specified by property flags. This structure is only for use with the 
    <a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a> function.


## -struct-fields




### -field Comment

Pointer to a null-terminated Unicode string that contains a comment associated with the DFS root or 
      link.


### -field State

Specifies a set of bit flags that describe the state of the DFS root or link; the state of the DFS 
      namespace root cannot be changed. One <b>DFS_VOLUME_STATE</b> flag is set, and one 
      <b>DFS_VOLUME_FLAVOR</b> flag is set. For an example that describes the interpretation of 
      these flags, see the Remarks section of 
      <a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a>.



#### Default (0x00000000)

Keep the existing state.



#### DFS_VOLUME_STATE_OK (0x00000001)

The specified DFS root or link is in the normal state.



#### DFS_VOLUME_STATE_OFFLINE (0x00000003)

The specified DFS root or link is offline or unavailable.



#### DFS_VOLUME_STATE_ONLINE (0x00000004)

The specified DFS root or link is available.


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
         independent of their site location. This flag applies to domain-based DFS roots, stand-alone roots, and 
         links. If this flag is set at the DFS root, it applies to all links; otherwise, it applies to an individual 
         link. Setting at the link does not override the root setting.



#### DFS_PROPERTY_FLAG_ROOT_SCALABILITY (0x00000002)

If this flag is set, the DFS server polls the nearest domain controller (DC) instead of the primary domain 
         controller (PDC) to check for DFS namespace changes for that namespace. Any modification to the DFS metadata 
         by the DFS server is not controlled by this flag but is sent to the PDC automatically. This flag applies to 
         the entire namespace and is valid only for domain-based DFS namespaces.



#### DFS_PROPERTY_FLAG_SITE_COSTING (0x00000004)

Set this flag to enable Active Directory site costing of targets. Targets returned from the DFS server to 
         the requesting DFS client are grouped by inter-site cost with respect to the DFS client. The groups are 
         ordered in terms of increasing site cost with first group consisting of targets in the same site as the 
         client. Targets within each group are ordered randomly.

If this flag is not enabled, the default return is two sets: one set of targets in the same site as the 
         client, and one set of all remaining targets. This flag applies to the entire DFS namespace and is valid for 
         both domain-based and stand-alone DFS namespaces.

Target priorities can further influence target ordering. For more information about how site-costing is 
         used to prioritize targets, see 
         <a href="https://msdn.microsoft.com/0aacebf7-49cc-4287-a5c4-0d25a416d227">DFS Server Target Prioritization</a>.



#### DFS_PROPERTY_FLAG_TARGET_FAILBACK (0x00000008)

Set this flag to enable V4 DFS clients to fail back to a more optimal (lower cost or higher priority) 
         target. If this flag is set at the DFS root, it applies to all links; otherwise, it applies to an individual 
         link. An individual link setting will not override a root setting. The target failback setting is provided to 
         the DFS client in a V4 referral response by the DFS server. This flag applies to domain-based DFS roots, 
         stand-alone roots, and links.



#### DFS_PROPERTY_FLAG_CLUSTER_ENABLED (0x00000010)

Scope: Stand-alone roots and links only.

If this flag is set, the DFS root is clustered to provide high 
         availability for storage failover. This flag cannot be set using the 
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


## -see-also




<a href="https://msdn.microsoft.com/0aacebf7-49cc-4287-a5c4-0d25a416d227">DFS Server Target Prioritization</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

