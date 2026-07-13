---
UID: NS:vds._VDS_PATH_POLICY
title: VDS_PATH_POLICY (vds.h)
description: The VDS_PATH_POLICY structure (vds.h) defines the load balance policy as it applies to a particular path. 
helpviewer_keywords: ["VDS_PATH_POLICY","VDS_PATH_POLICY structure [VDS]","base.vds_path_policy","vds/VDS_PATH_POLICY","vdshwprv/VDS_PATH_POLICY"]
old-location: base\vds_path_policy.htm
tech.root: base
ms.assetid: 7dec1d91-6781-42fa-9476-bb64e2554017
ms.date: 08/05/2022
ms.keywords: VDS_PATH_POLICY, VDS_PATH_POLICY structure [VDS], base.vds_path_policy, vds/VDS_PATH_POLICY, vdshwprv/VDS_PATH_POLICY
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
req.typenames: VDS_PATH_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PATH_POLICY
 - vds/_VDS_PATH_POLICY
 - VDS_PATH_POLICY
 - vds/VDS_PATH_POLICY
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
 - VDS_PATH_POLICY
---

# VDS_PATH_POLICY structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
    load balance policy as it applies to a particular path.

## -struct-fields

### -field pathId

The ID of the path used by MPIO.

### -field bPrimaryPath

If set, indicates that the path is a primary path for MPIO.

### -field ulWeight

The weight assigned to the path. This is only relevant if the load balance policy for the LUN is 
      <b>VDS_LBP_WEIGHTED_PATHS</b>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getloadbalancepolicy">IVdsLunMpio::GetLoadBalancePolicy</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-setloadbalancepolicy">IVdsLunMpio::SetLoadBalancePolicy</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>
