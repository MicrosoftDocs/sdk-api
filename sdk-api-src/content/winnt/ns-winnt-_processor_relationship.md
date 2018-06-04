---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _PROCESSOR_RELATIONSHIP structure


## -description


Represents information about affinity within a processor group. This structure is used with the <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function.


## -struct-fields




### -field Flags

If the <b>Relationship</b> member of the <a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorCore</b>, this member is LTP_PC_SMT if the core has more than one logical processor, or 0 if the core has one logical processor. 

If the <b>Relationship</b> member of the <a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorPackage</b>, this member is always 0.


### -field EfficiencyClass

 If the <b>Relationship</b> member of the <a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorCore</b>, <b>EfficiencyClass</b> specifies the intrinsic tradeoff between performance and power for the applicable core. A core  with a higher value for the efficiency class has intrinsically greater performance and less efficiency than a core with a lower value for the efficiency class. <b>EfficiencyClass</b> is only nonzero on systems with a heterogeneous set of cores.

If the <b>Relationship</b> member of the <a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a> structure is <b>RelationProcessorPackage</b>, <b>EfficiencyClass</b> is always 0.

The minimum operating system version that supports this member is Windows 10.


### -field Reserved

This member is reserved.


### -field GroupCount

This member specifies the number of entries in the <b>GroupMask</b> array. For more information, see Remarks.


### -field GroupMask

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff546539">GROUP_AFFINITY</a> structures. The <b>GroupCount</b> member specifies the number of structures in the array. Each structure in the array specifies a  group number and processor affinity within the group. 


## -remarks



The <b>PROCESSOR_RELATIONSHIP</b> structure describes the logical processors associated with either a processor core or a processor package.  

If the <b>PROCESSOR_RELATIONSHIP</b> structure represents a processor core, the <b>GroupCount</b> member is always 1.  

If the <b>PROCESSOR_RELATIONSHIP</b> structure represents a processor package, the  <b>GroupCount</b> member is 1 only if all processors are in the same processor group. If the package contains more than one NUMA node, the system might assign different NUMA nodes to different processor groups. In this case, the <b>GroupCount</b> member is the number of groups to which NUMA nodes in the package are assigned. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546539">GROUP_AFFINITY</a>



<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

