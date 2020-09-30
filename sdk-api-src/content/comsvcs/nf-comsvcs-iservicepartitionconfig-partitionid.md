---
UID: NF:comsvcs.IServicePartitionConfig.PartitionID
title: IServicePartitionConfig::PartitionID (comsvcs.h)
description: Sets the GUID for the partition that is used for the enclosed work.
helpviewer_keywords: ["IServicePartitionConfig interface [COM+]","PartitionID method","IServicePartitionConfig.PartitionID","IServicePartitionConfig::PartitionID","PartitionID","PartitionID method [COM+]","PartitionID method [COM+]","IServicePartitionConfig interface","_cos_IServicePartitionConfig_PartitionID","comsvcs/IServicePartitionConfig::PartitionID","cos.iservicepartitionconfig_partitionid"]
old-location: cos\iservicepartitionconfig_partitionid.htm
tech.root: cos
ms.assetid: 40480925-dfb6-40ea-a8ea-72659e359b47
ms.date: 12/05/2018
ms.keywords: IServicePartitionConfig interface [COM+],PartitionID method, IServicePartitionConfig.PartitionID, IServicePartitionConfig::PartitionID, PartitionID, PartitionID method [COM+], PartitionID method [COM+],IServicePartitionConfig interface, _cos_IServicePartitionConfig_PartitionID, comsvcs/IServicePartitionConfig::PartitionID, cos.iservicepartitionconfig_partitionid
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
 - IServicePartitionConfig::PartitionID
 - comsvcs/IServicePartitionConfig::PartitionID
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
 - IServicePartitionConfig.PartitionID
---

# IServicePartitionConfig::PartitionID


## -description

Sets the GUID for the partition that is used for the enclosed work.

## -parameters

### -param guidPartitionID [in]

A GUID that is used to specify the partition that is to be used to run the enclosed work.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicepartitionconfig">IServicePartitionConfig</a>