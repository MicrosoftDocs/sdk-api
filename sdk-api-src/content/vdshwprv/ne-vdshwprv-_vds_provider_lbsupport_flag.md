---
UID: NE:vdshwprv._VDS_PROVIDER_LBSUPPORT_FLAG
title: "_VDS_PROVIDER_LBSUPPORT_FLAG"
author: windows-driver-content
description: Specifies the set of valid flags for indicating which load balance policies a hardware provider supports.
old-location: base\vds_provider_lbsupport_flag.htm
old-project: VDS
ms.assetid: bfc9aabf-b9ce-4b36-b68a-b74628092962
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: VDS_LBF_DYN_LEAST_QUEUE_DEPTH, VDS_LBF_FAILOVER, VDS_LBF_LEAST_BLOCKS, VDS_LBF_ROUND_ROBIN, VDS_LBF_ROUND_ROBIN_WITH_SUBSET, VDS_LBF_VENDOR_SPECIFIC, VDS_LBF_WEIGHTED_PATHS, VDS_PROVIDER_LBSUPPORT_FLAG, VDS_PROVIDER_LBSUPPORT_FLAG enumeration [VDS], _VDS_PROVIDER_LBSUPPORT_FLAG, base.vds_provider_lbsupport_flag, vds/VDS_LBF_DYN_LEAST_QUEUE_DEPTH, vds/VDS_LBF_FAILOVER, vds/VDS_LBF_LEAST_BLOCKS, vds/VDS_LBF_ROUND_ROBIN, vds/VDS_LBF_ROUND_ROBIN_WITH_SUBSET, vds/VDS_LBF_VENDOR_SPECIFIC, vds/VDS_LBF_WEIGHTED_PATHS, vds/VDS_PROVIDER_LBSUPPORT_FLAG, vdshwprv/VDS_LBF_DYN_LEAST_QUEUE_DEPTH, vdshwprv/VDS_LBF_FAILOVER, vdshwprv/VDS_LBF_LEAST_BLOCKS, vdshwprv/VDS_LBF_ROUND_ROBIN, vdshwprv/VDS_LBF_ROUND_ROBIN_WITH_SUBSET, vdshwprv/VDS_LBF_VENDOR_SPECIFIC, vdshwprv/VDS_LBF_WEIGHTED_PATHS, vdshwprv/VDS_PROVIDER_LBSUPPORT_FLAG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vdshwprv.h
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
req.typenames: VDS_PROVIDER_LBSUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_PROVIDER_LBSUPPORT_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_PROVIDER_LBSUPPORT_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Specifies the set of valid flags for indicating which load balance policies a hardware provider 
    supports.


## -enum-fields




### -field VDS_LBF_FAILOVER

The provider supports using one primary path with the other paths being backup paths.


### -field VDS_LBF_ROUND_ROBIN

The provider supports using all paths in round robin fashion.


### -field VDS_LBF_ROUND_ROBIN_WITH_SUBSET

The provider supports using primary paths in round robin fashion. The backup paths are used if all of the 
      primary paths fail.


### -field VDS_LBF_DYN_LEAST_QUEUE_DEPTH

The provider supports using the path with the least number of active requests.


### -field VDS_LBF_WEIGHTED_PATHS

The provider supports using the path with the least weight (each path is assigned a weight).


### -field VDS_LBF_LEAST_BLOCKS

The provider supports using the path with the least blocks.


### -field VDS_LBF_VENDOR_SPECIFIC

The provider supports a vendor-specific policy.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PROVIDER_LBSUPPORT_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PROVIDER_LBSUPPORT_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

