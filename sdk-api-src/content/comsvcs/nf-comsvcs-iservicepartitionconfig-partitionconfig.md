---
UID: NF:comsvcs.IServicePartitionConfig.PartitionConfig
title: IServicePartitionConfig::PartitionConfig (comsvcs.h)
description: Configures how partitions are used for the enclosed work.
helpviewer_keywords: ["IServicePartitionConfig interface [COM+]","PartitionConfig method","IServicePartitionConfig.PartitionConfig","IServicePartitionConfig::PartitionConfig","PartitionConfig","PartitionConfig method [COM+]","PartitionConfig method [COM+]","IServicePartitionConfig interface","_cos_IServicePartitionConfig_PartitionConfig","comsvcs/IServicePartitionConfig::PartitionConfig","cos.iservicepartitionconfig_partitionconfig"]
old-location: cos\iservicepartitionconfig_partitionconfig.htm
tech.root: cos
ms.assetid: 0f8c5353-5740-4c7e-91be-f336424fb93a
ms.date: 12/05/2018
ms.keywords: IServicePartitionConfig interface [COM+],PartitionConfig method, IServicePartitionConfig.PartitionConfig, IServicePartitionConfig::PartitionConfig, PartitionConfig, PartitionConfig method [COM+], PartitionConfig method [COM+],IServicePartitionConfig interface, _cos_IServicePartitionConfig_PartitionConfig, comsvcs/IServicePartitionConfig::PartitionConfig, cos.iservicepartitionconfig_partitionconfig
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServicePartitionConfig::PartitionConfig
 - comsvcs/IServicePartitionConfig::PartitionConfig
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServicePartitionConfig.PartitionConfig
---

# IServicePartitionConfig::PartitionConfig


## -description

Configures how partitions are used for the enclosed work.

## -parameters

### -param partitionConfig [in]

A value from the <a href="/windows/desktop/api/comsvcs/ne-comsvcs-csc_partitionconfig">CSC_PartitionConfig</a> enumeration.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -remarks

The user must belong to any partition that is used to run the enclosed work.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepartitionconfig">IServicePartitionConfig</a>