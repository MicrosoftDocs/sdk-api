---
UID: NS:winnt._NUMA_NODE_RELATIONSHIP
title: "_NUMA_NODE_RELATIONSHIP"
author: windows-driver-content
description: Represents information about a NUMA node in a processor group. This structure is used with the GetLogicalProcessorInformationEx function.
old-location: base\numa_node_relationship.htm
old-project: ProcThread
ms.assetid: a4e4c994-c4af-4b4f-8684-6037bcba35a9
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*PNUMA_NODE_RELATIONSHIP, NUMA_NODE_RELATIONSHIP, NUMA_NODE_RELATIONSHIP structure, PNUMA_NODE_RELATIONSHIP, PNUMA_NODE_RELATIONSHIP structure pointer, _NUMA_NODE_RELATIONSHIP, base.numa_node_relationship, winnt/NUMA_NODE_RELATIONSHIP, winnt/PNUMA_NODE_RELATIONSHIP"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: NUMA_NODE_RELATIONSHIP, *PNUMA_NODE_RELATIONSHIP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinNT.h
api_name:
-	NUMA_NODE_RELATIONSHIP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _NUMA_NODE_RELATIONSHIP structure


## -description


Represents information about a NUMA node in a processor group. This structure is used with the <a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a> function.


## -struct-fields




### -field NodeNumber

The number of the NUMA node.


### -field Reserved

This member is reserved.


### -field GroupMask

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff546539">GROUP_AFFINITY</a> structure that specifies a  group number and processor affinity within the group. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546539">GROUP_AFFINITY</a>



<a href="https://msdn.microsoft.com/dfc4f444-4651-4a02-b8f6-f30d9278eae2">GetLogicalProcessorInformationEx</a>



<a href="https://msdn.microsoft.com/6ff16cda-c1dc-4d5c-ac60-756653cd6b07">SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX</a>
 

 

