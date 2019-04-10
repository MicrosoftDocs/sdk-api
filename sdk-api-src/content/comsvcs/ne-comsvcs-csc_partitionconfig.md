---
UID: NE:comsvcs.tagCSC_PartitionConfig
title: CSC_PartitionConfig (comsvcs.h)
author: windows-sdk-content
description: Indicates the COM+ partition on which the enclosed context runs.
old-location: cos\csc_partitionconfig.htm
tech.root: cossdk
ms.assetid: 584c4744-193d-43d4-a305-8f4ea9802d58
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CSC_InheritPartition, CSC_NewPartition, CSC_NoPartition, CSC_PartitionConfig, CSC_PartitionConfig enumeration [COM+], _cos_CSC_PartitionConfig, comsvcs/CSC_InheritPartition, comsvcs/CSC_NewPartition, comsvcs/CSC_NoPartition, comsvcs/CSC_PartitionConfig, cos.csc_partitionconfig
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_PartitionConfig
product: Windows
targetos: Windows
req.typenames: CSC_PartitionConfig
req.redist: 
---

# CSC_PartitionConfig enumeration


## -description


Indicates the COM+ partition on which the enclosed context runs.


## -enum-fields




### -field CSC_NoPartition

The enclosed context runs on the Base Application Partition. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_InheritPartition

The enclosed context runs in the current containing COM+ partition. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/9bc8c4f3-d13e-46b6-9187-904b05f66f66">CSC_InheritanceConfig</a> is set to CSC_Inherit.


### -field CSC_NewPartition

The enclosed context runs in a COM+ partition that is different from the current containing partition.



## -remarks



This enumeration is used to specify the working COM+ partition through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/b67b3cf6-4462-4578-b61b-c5c61d809822">CoLeaveServiceDomain</a>.




## -see-also




<a href="https://msdn.microsoft.com/fd22a64c-f2d8-48af-86e1-985e21b0f8fa">COM+ Partitions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/0f8c5353-5740-4c7e-91be-f336424fb93a">IServicePartitionConfig::PartitionConfig</a>
 

 

