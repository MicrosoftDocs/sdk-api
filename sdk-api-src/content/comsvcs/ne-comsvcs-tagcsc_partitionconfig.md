---
UID: NE:comsvcs.tagCSC_PartitionConfig
title: tagCSC_PartitionConfig
author: windows-sdk-content
description: Indicates the COM+ partition on which the enclosed context runs.
old-location: cos\csc_partitionconfig.htm
tech.root: cossdk
ms.assetid: 584c4744-193d-43d4-a305-8f4ea9802d58
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CSC_InheritPartition, CSC_NewPartition, CSC_NoPartition, CSC_PartitionConfig, CSC_PartitionConfig enumeration [COM+], _cos_CSC_PartitionConfig, comsvcs/CSC_InheritPartition, comsvcs/CSC_NewPartition, comsvcs/CSC_NoPartition, comsvcs/CSC_PartitionConfig, cos.csc_partitionconfig, tagCSC_PartitionConfig
ms.prod: windows-hardware
ms.technology: windows-devices
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

# tagCSC_PartitionConfig enumeration


## -description


Indicates the COM+ partition on which the enclosed context runs.


## -enum-fields




### -field CSC_NoPartition

The enclosed context runs on the Base Application Partition. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/en-us/library/ms684375(v=VS.85).aspx">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_InheritPartition

The enclosed context runs in the current containing COM+ partition. This is the default setting for <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> when <a href="https://msdn.microsoft.com/en-us/library/ms684375(v=VS.85).aspx">CSC_InheritanceConfig</a> is set to CSC_Inherit.


### -field CSC_NewPartition

The enclosed context runs in a COM+ partition that is different from the current containing partition.



## -remarks



This enumeration is used to specify the working COM+ partition through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/en-us/library/ms686062(v=VS.85).aspx">CoLeaveServiceDomain</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688501(v=VS.85).aspx">COM+ Partitions</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678943(v=VS.85).aspx">IServicePartitionConfig::PartitionConfig</a>
 

 

