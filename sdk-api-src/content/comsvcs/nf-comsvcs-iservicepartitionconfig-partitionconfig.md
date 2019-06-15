---
UID: NF:comsvcs.IServicePartitionConfig.PartitionConfig
title: IServicePartitionConfig::PartitionConfig (comsvcs.h)
author: windows-sdk-content
description: Configures how partitions are used for the enclosed work.
old-location: cos\iservicepartitionconfig_partitionconfig.htm
tech.root: cossdk
ms.assetid: 0f8c5353-5740-4c7e-91be-f336424fb93a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IServicePartitionConfig interface [COM+],PartitionConfig method, IServicePartitionConfig.PartitionConfig, IServicePartitionConfig::PartitionConfig, PartitionConfig, PartitionConfig method [COM+], PartitionConfig method [COM+],IServicePartitionConfig interface, _cos_IServicePartitionConfig_PartitionConfig, comsvcs/IServicePartitionConfig::PartitionConfig, cos.iservicepartitionconfig_partitionconfig
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServicePartitionConfig.PartitionConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServicePartitionConfig::PartitionConfig


## -description


Configures how partitions are used for the enclosed work.


## -parameters




### -param partitionConfig [in]

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ne-comsvcs-tagcsc_partitionconfig">CSC_PartitionConfig</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



The user must belong to any partition that is used to run the enclosed work.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicepartitionconfig">IServicePartitionConfig</a>
 

 

