---
UID: NE:vds._VDS_LOADBALANCE_POLICY_ENUM
title: VDS_LOADBALANCE_POLICY_ENUM (vds.h)
description: Defines a set of valid load balance policies for a path.
helpviewer_keywords: ["VDS_LBP_DYN_LEAST_QUEUE_DEPTH","VDS_LBP_FAILOVER","VDS_LBP_LEAST_BLOCKS","VDS_LBP_ROUND_ROBIN","VDS_LBP_ROUND_ROBIN_WITH_SUBSET","VDS_LBP_UNKNOWN","VDS_LBP_VENDOR_SPECIFIC","VDS_LBP_WEIGHTED_PATHS","VDS_LOADBALANCE_POLICY_ENUM","VDS_LOADBALANCE_POLICY_ENUM enumeration [VDS]","base.vds_loadbalance_policy_enum","vds/VDS_LBP_DYN_LEAST_QUEUE_DEPTH","vds/VDS_LBP_FAILOVER","vds/VDS_LBP_LEAST_BLOCKS","vds/VDS_LBP_ROUND_ROBIN","vds/VDS_LBP_ROUND_ROBIN_WITH_SUBSET","vds/VDS_LBP_UNKNOWN","vds/VDS_LBP_VENDOR_SPECIFIC","vds/VDS_LBP_WEIGHTED_PATHS","vds/VDS_LOADBALANCE_POLICY_ENUM","vdshwprv/VDS_LBP_DYN_LEAST_QUEUE_DEPTH","vdshwprv/VDS_LBP_FAILOVER","vdshwprv/VDS_LBP_LEAST_BLOCKS","vdshwprv/VDS_LBP_ROUND_ROBIN","vdshwprv/VDS_LBP_ROUND_ROBIN_WITH_SUBSET","vdshwprv/VDS_LBP_UNKNOWN","vdshwprv/VDS_LBP_VENDOR_SPECIFIC","vdshwprv/VDS_LBP_WEIGHTED_PATHS","vdshwprv/VDS_LOADBALANCE_POLICY_ENUM"]
old-location: base\vds_loadbalance_policy_enum.htm
tech.root: base
ms.assetid: 0391c605-3808-4c24-8638-77b1fe3342bf
ms.date: 12/05/2018
ms.keywords: VDS_LBP_DYN_LEAST_QUEUE_DEPTH, VDS_LBP_FAILOVER, VDS_LBP_LEAST_BLOCKS, VDS_LBP_ROUND_ROBIN, VDS_LBP_ROUND_ROBIN_WITH_SUBSET, VDS_LBP_UNKNOWN, VDS_LBP_VENDOR_SPECIFIC, VDS_LBP_WEIGHTED_PATHS, VDS_LOADBALANCE_POLICY_ENUM, VDS_LOADBALANCE_POLICY_ENUM enumeration [VDS], base.vds_loadbalance_policy_enum, vds/VDS_LBP_DYN_LEAST_QUEUE_DEPTH, vds/VDS_LBP_FAILOVER, vds/VDS_LBP_LEAST_BLOCKS, vds/VDS_LBP_ROUND_ROBIN, vds/VDS_LBP_ROUND_ROBIN_WITH_SUBSET, vds/VDS_LBP_UNKNOWN, vds/VDS_LBP_VENDOR_SPECIFIC, vds/VDS_LBP_WEIGHTED_PATHS, vds/VDS_LOADBALANCE_POLICY_ENUM, vdshwprv/VDS_LBP_DYN_LEAST_QUEUE_DEPTH, vdshwprv/VDS_LBP_FAILOVER, vdshwprv/VDS_LBP_LEAST_BLOCKS, vdshwprv/VDS_LBP_ROUND_ROBIN, vdshwprv/VDS_LBP_ROUND_ROBIN_WITH_SUBSET, vdshwprv/VDS_LBP_UNKNOWN, vdshwprv/VDS_LBP_VENDOR_SPECIFIC, vdshwprv/VDS_LBP_WEIGHTED_PATHS, vdshwprv/VDS_LOADBALANCE_POLICY_ENUM
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: VDS_LOADBALANCE_POLICY_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LOADBALANCE_POLICY_ENUM
 - vds/_VDS_LOADBALANCE_POLICY_ENUM
 - VDS_LOADBALANCE_POLICY_ENUM
 - vds/VDS_LOADBALANCE_POLICY_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_LOADBALANCE_POLICY_ENUM
---

# VDS_LOADBALANCE_POLICY_ENUM enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a set of valid load balance policies for a path. These policies correspond to the 
   definitions in the DSM MOF.

## -enum-fields

### -field VDS_LBP_UNKNOWN:0

The policy is unknown.

### -field VDS_LBP_FAILOVER:1

The policy uses one primary path with other paths being backup paths.

### -field VDS_LBP_ROUND_ROBIN:2

The policy uses all paths in round-robin fashion.

### -field VDS_LBP_ROUND_ROBIN_WITH_SUBSET:3

The policy uses primary paths in round-robin fashion. The backup paths are used if all of the primary paths 
     fail.

### -field VDS_LBP_DYN_LEAST_QUEUE_DEPTH:4

The policy uses the path with the least number of active requests.

### -field VDS_LBP_WEIGHTED_PATHS:5

The policy uses the path with the least weight (each path is assigned a weight).

### -field VDS_LBP_LEAST_BLOCKS:6

The policy uses the path with the least blocks.

### -field VDS_LBP_VENDOR_SPECIFIC:7

The policy is a vendor-specific policy.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LOADBALANCE_POLICY_ENUM</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LOADBALANCE_POLICY_ENUM</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
