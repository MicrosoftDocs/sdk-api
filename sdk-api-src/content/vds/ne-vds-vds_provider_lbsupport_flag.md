---
UID: NE:vds._VDS_PROVIDER_LBSUPPORT_FLAG
title: VDS_PROVIDER_LBSUPPORT_FLAG (vds.h)
description: Specifies the set of valid flags for indicating which load balance policies a hardware provider supports.
helpviewer_keywords: ["VDS_LBF_DYN_LEAST_QUEUE_DEPTH","VDS_LBF_FAILOVER","VDS_LBF_LEAST_BLOCKS","VDS_LBF_ROUND_ROBIN","VDS_LBF_ROUND_ROBIN_WITH_SUBSET","VDS_LBF_VENDOR_SPECIFIC","VDS_LBF_WEIGHTED_PATHS","VDS_PROVIDER_LBSUPPORT_FLAG","VDS_PROVIDER_LBSUPPORT_FLAG enumeration [VDS]","base.vds_provider_lbsupport_flag","vds/VDS_LBF_DYN_LEAST_QUEUE_DEPTH","vds/VDS_LBF_FAILOVER","vds/VDS_LBF_LEAST_BLOCKS","vds/VDS_LBF_ROUND_ROBIN","vds/VDS_LBF_ROUND_ROBIN_WITH_SUBSET","vds/VDS_LBF_VENDOR_SPECIFIC","vds/VDS_LBF_WEIGHTED_PATHS","vds/VDS_PROVIDER_LBSUPPORT_FLAG","vdshwprv/VDS_LBF_DYN_LEAST_QUEUE_DEPTH","vdshwprv/VDS_LBF_FAILOVER","vdshwprv/VDS_LBF_LEAST_BLOCKS","vdshwprv/VDS_LBF_ROUND_ROBIN","vdshwprv/VDS_LBF_ROUND_ROBIN_WITH_SUBSET","vdshwprv/VDS_LBF_VENDOR_SPECIFIC","vdshwprv/VDS_LBF_WEIGHTED_PATHS","vdshwprv/VDS_PROVIDER_LBSUPPORT_FLAG"]
old-location: base\vds_provider_lbsupport_flag.htm
tech.root: base
ms.assetid: bfc9aabf-b9ce-4b36-b68a-b74628092962
ms.date: 12/05/2018
ms.keywords: VDS_LBF_DYN_LEAST_QUEUE_DEPTH, VDS_LBF_FAILOVER, VDS_LBF_LEAST_BLOCKS, VDS_LBF_ROUND_ROBIN, VDS_LBF_ROUND_ROBIN_WITH_SUBSET, VDS_LBF_VENDOR_SPECIFIC, VDS_LBF_WEIGHTED_PATHS, VDS_PROVIDER_LBSUPPORT_FLAG, VDS_PROVIDER_LBSUPPORT_FLAG enumeration [VDS], base.vds_provider_lbsupport_flag, vds/VDS_LBF_DYN_LEAST_QUEUE_DEPTH, vds/VDS_LBF_FAILOVER, vds/VDS_LBF_LEAST_BLOCKS, vds/VDS_LBF_ROUND_ROBIN, vds/VDS_LBF_ROUND_ROBIN_WITH_SUBSET, vds/VDS_LBF_VENDOR_SPECIFIC, vds/VDS_LBF_WEIGHTED_PATHS, vds/VDS_PROVIDER_LBSUPPORT_FLAG, vdshwprv/VDS_LBF_DYN_LEAST_QUEUE_DEPTH, vdshwprv/VDS_LBF_FAILOVER, vdshwprv/VDS_LBF_LEAST_BLOCKS, vdshwprv/VDS_LBF_ROUND_ROBIN, vdshwprv/VDS_LBF_ROUND_ROBIN_WITH_SUBSET, vdshwprv/VDS_LBF_VENDOR_SPECIFIC, vdshwprv/VDS_LBF_WEIGHTED_PATHS, vdshwprv/VDS_PROVIDER_LBSUPPORT_FLAG
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
req.typenames: VDS_PROVIDER_LBSUPPORT_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PROVIDER_LBSUPPORT_FLAG
 - vds/_VDS_PROVIDER_LBSUPPORT_FLAG
 - VDS_PROVIDER_LBSUPPORT_FLAG
 - vds/VDS_PROVIDER_LBSUPPORT_FLAG
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
 - VDS_PROVIDER_LBSUPPORT_FLAG
---

# VDS_PROVIDER_LBSUPPORT_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Specifies the set of valid flags for indicating which load balance policies a hardware provider 
    supports.

## -enum-fields

### -field VDS_LBF_FAILOVER:0x1

The provider supports using one primary path with the other paths being backup paths.

### -field VDS_LBF_ROUND_ROBIN:0x2

The provider supports using all paths in round robin fashion.

### -field VDS_LBF_ROUND_ROBIN_WITH_SUBSET:0x4

The provider supports using primary paths in round robin fashion. The backup paths are used if all of the 
      primary paths fail.

### -field VDS_LBF_DYN_LEAST_QUEUE_DEPTH:0x8

The provider supports using the path with the least number of active requests.

### -field VDS_LBF_WEIGHTED_PATHS:0x10

The provider supports using the path with the least weight (each path is assigned a weight).

### -field VDS_LBF_LEAST_BLOCKS:0x20

The provider supports using the path with the least blocks.

### -field VDS_LBF_VENDOR_SPECIFIC:0x40

The provider supports a vendor-specific policy.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PROVIDER_LBSUPPORT_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PROVIDER_LBSUPPORT_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
