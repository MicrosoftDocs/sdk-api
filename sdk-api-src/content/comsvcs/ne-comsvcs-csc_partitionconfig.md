---
UID: NE:comsvcs.tagCSC_PartitionConfig
title: CSC_PartitionConfig (comsvcs.h)
description: Indicates the COM+ partition on which the enclosed context runs.
helpviewer_keywords: ["CSC_InheritPartition","CSC_NewPartition","CSC_NoPartition","CSC_PartitionConfig","CSC_PartitionConfig enumeration [COM+]","_cos_CSC_PartitionConfig","comsvcs/CSC_InheritPartition","comsvcs/CSC_NewPartition","comsvcs/CSC_NoPartition","comsvcs/CSC_PartitionConfig","cos.csc_partitionconfig"]
old-location: cos\csc_partitionconfig.htm
tech.root: cos
ms.assetid: 584c4744-193d-43d4-a305-8f4ea9802d58
ms.date: 12/05/2018
ms.keywords: CSC_InheritPartition, CSC_NewPartition, CSC_NoPartition, CSC_PartitionConfig, CSC_PartitionConfig enumeration [COM+], _cos_CSC_PartitionConfig, comsvcs/CSC_InheritPartition, comsvcs/CSC_NewPartition, comsvcs/CSC_NoPartition, comsvcs/CSC_PartitionConfig, cos.csc_partitionconfig
req.header: comsvcs.h
req.include-header: 
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
req.typenames: CSC_PartitionConfig
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCSC_PartitionConfig
 - comsvcs/tagCSC_PartitionConfig
 - CSC_PartitionConfig
 - comsvcs/CSC_PartitionConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_PartitionConfig
---

# CSC_PartitionConfig enumeration


## -description

Indicates the COM+ partition on which the enclosed context runs.

## -enum-fields

### -field CSC_NoPartition:0

The enclosed context runs on the Base Application Partition. This is the default setting for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Ignore.

### -field CSC_InheritPartition

The enclosed context runs in the current containing COM+ partition. This is the default setting for <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Inherit.

### -field CSC_NewPartition

The enclosed context runs in a COM+ partition that is different from the current containing partition.

## -remarks

This enumeration is used to specify the working COM+ partition through <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> for either the work submitted through the activity created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or the work that is enclosed between calls to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>.

## -see-also

<a href="/windows/desktop/cossdk/com--partitions">COM+ Partitions</a>



<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicepartitionconfig-partitionconfig">IServicePartitionConfig::PartitionConfig</a>
