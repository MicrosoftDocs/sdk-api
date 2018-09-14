---
UID: NN:comsvcs.IServicePartitionConfig
title: IServicePartitionConfig
author: windows-sdk-content
description: Configures how partitions are used for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicepartitionconfig.htm
tech.root: cossdk
ms.assetid: 63dcc64b-edd5-4188-a87b-46452c3b624f
ms.author: windowssdkdev
ms.date: 08/31/2018
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServicePartitionConfig interface


## -description


Configures how partitions are used for the work that is done when calling either <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServicePartitionConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IServicePartitionConfig</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms678943(v=VS.85).aspx">PartitionConfig</a>
</td>
<td align="left" width="63%">
Configures how partitions are used for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680598(v=VS.85).aspx">PartitionID</a>
</td>
<td align="left" width="63%">
Sets the GUID for the partition that is used for the enclosed work.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688501(v=VS.85).aspx">COM+ Partitions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

