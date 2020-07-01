---
UID: NN:comsvcs.IServicePartitionConfig
title: IServicePartitionConfig (comsvcs.h)
description: Configures how partitions are used for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
helpviewer_keywords: ["IServicePartitionConfig","IServicePartitionConfig interface [COM+]","IServicePartitionConfig interface [COM+]","described","_cos_IServicePartitionConfi","comsvcs/IServicePartitionConfig","cos.iservicepartitionconfig"]
old-location: cos\iservicepartitionconfig.htm
tech.root: cossdk
ms.assetid: 63dcc64b-edd5-4188-a87b-46452c3b624f
ms.date: 12/05/2018
ms.keywords: IServicePartitionConfig, IServicePartitionConfig interface [COM+], IServicePartitionConfig interface [COM+],described, _cos_IServicePartitionConfi, comsvcs/IServicePartitionConfig, cos.iservicepartitionconfig
f1_keywords:
- comsvcs/IServicePartitionConfig
dev_langs:
- c++
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
- IServicePartitionConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServicePartitionConfig interface


## -description


Configures how partitions are used for the work that is done when calling either <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServicePartitionConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServicePartitionConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServicePartitionConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepartitionconfig-partitionconfig">PartitionConfig</a>
</td>
<td align="left" width="63%">
Configures how partitions are used for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepartitionconfig-partitionid">PartitionID</a>
</td>
<td align="left" width="63%">
Sets the GUID for the partition that is used for the enclosed work.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--partitions">COM+ Partitions</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>
 

 

