---
UID: NN:comsvcs.IServicePartitionConfig
title: IServicePartitionConfig
author: windows-sdk-content
description: Configures how partitions are used for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicepartitionconfig.htm
old-project: cossdk
ms.assetid: 63dcc64b-edd5-4188-a87b-46452c3b624f
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IServicePartitionConfig, IServicePartitionConfig interface [COM+], IServicePartitionConfig interface [COM+],described, _cos_IServicePartitionConfi, comsvcs/IServicePartitionConfig, cos.iservicepartitionconfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServicePartitionConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServicePartitionConfig interface


## -description


Configures how partitions are used for the work that is done when calling either <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServicePartitionConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServicePartitionConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0f8c5353-5740-4c7e-91be-f336424fb93a">PartitionConfig</a>
</td>
<td align="left" width="63%">
Configures how partitions are used for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn915683">PartitionID</a>
</td>
<td align="left" width="63%">
Sets the GUID for the partition that is used for the enclosed work.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fd22a64c-f2d8-48af-86e1-985e21b0f8fa">COM+ Partitions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

