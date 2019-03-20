---
UID: NS:winnt._NUMA_NODE_RELATIONSHIP
title: NUMA_NODE_RELATIONSHIP (winnt.h)
author: windows-sdk-content
description: Represents information about a NUMA node in a processor group. This structure is used with the GetLogicalProcessorInformationEx function.
old-location: base\numa_node_relationship.htm
tech.root: ProcThread
ms.assetid: a4e4c994-c4af-4b4f-8684-6037bcba35a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PNUMA_NODE_RELATIONSHIP, NUMA_NODE_RELATIONSHIP, NUMA_NODE_RELATIONSHIP structure, PNUMA_NODE_RELATIONSHIP, PNUMA_NODE_RELATIONSHIP structure pointer, _NUMA_NODE_RELATIONSHIP, base.numa_node_relationship, winnt/NUMA_NODE_RELATIONSHIP, winnt/PNUMA_NODE_RELATIONSHIP"
ms.topic: struct
req.header: winnt.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - NUMA_NODE_RELATIONSHIP
product: Windows
targetos: Windows
req.typenames: NUMA_NODE_RELATIONSHIP, *PNUMA_NODE_RELATIONSHIP
req.redist: 
---

# NUMA_NODE_RELATIONSHIP structure


## -description


Represents information about a NUMA node in a processor group. This structure is used with the <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function.


## -struct-fields




### -field NodeNumber

The number of the NUMA node.


### -field Reserved

This member is reserved.


### -field GroupMask

A <a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a> structure that specifies a  group number and processor affinity within the group. 


## -see-also




<a href="https://msdn.microsoft.com/76009431-9139-4c03-9c7b-0c4bb5f0cb83">GROUP_AFFINITY</a>



<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd405522(v=VS.85).aspx">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

