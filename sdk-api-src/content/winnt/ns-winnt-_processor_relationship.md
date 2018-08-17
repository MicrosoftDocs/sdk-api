---
UID: NS:winnt._PROCESSOR_RELATIONSHIP
title: "_PROCESSOR_RELATIONSHIP"
author: windows-sdk-content
description: Represents information about affinity within a processor group. This structure is used with the GetLogicalProcessorInformationEx function.
old-location: base\processor_relationship.htm
old-project: procthread
ms.assetid: 1efda80d-cf5b-4312-801a-ea3585b152ac
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PPROCESSOR_RELATIONSHIP, PPROCESSOR_RELATIONSHIP, PPROCESSOR_RELATIONSHIP structure pointer, PROCESSOR_RELATIONSHIP, PROCESSOR_RELATIONSHIP structure, _PROCESSOR_RELATIONSHIP, base.processor_relationship, winnt/PPROCESSOR_RELATIONSHIP, winnt/PROCESSOR_RELATIONSHIP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PROCESSOR_RELATIONSHIP, *PPROCESSOR_RELATIONSHIP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - PROCESSOR_RELATIONSHIP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

An array of <a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a> structures. The <b>GroupCount</b> member specifies the number of structures in the array. Each structure in the array specifies a  group number and processor affinity within the group. 


## -remarks



The <b>PROCESSOR_RELATIONSHIP</b> structure describes the logical processors associated with either a processor core or a processor package.  

If the <b>PROCESSOR_RELATIONSHIP</b> structure represents a processor core, the <b>GroupCount</b> member is always 1.  

If the <b>PROCESSOR_RELATIONSHIP</b> structure represents a processor package, the  <b>GroupCount</b> member is 1 only if all processors are in the same processor group. If the package contains more than one NUMA node, the system might assign different NUMA nodes to different processor groups. In this case, the <b>GroupCount</b> member is the number of groups to which NUMA nodes in the package are assigned. 




## -see-also




<a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a>



<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

