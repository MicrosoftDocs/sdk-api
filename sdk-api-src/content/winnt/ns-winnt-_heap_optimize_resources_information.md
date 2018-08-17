---
UID: NS:winnt._HEAP_OPTIMIZE_RESOURCES_INFORMATION
title: "_HEAP_OPTIMIZE_RESOURCES_INFORMATION"
author: windows-sdk-content
description: Specifies flags for a HeapOptimizeResources operation initiated with HeapSetInformation.
old-location: base\heap_optimize_resources_information.htm
old-project: memory
ms.assetid: c801a08a-0b1a-4ffe-8ec7-c3ea8d913ec8
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PHEAP_OPTIMIZE_RESOURCES_INFORMATION, HEAP_OPTIMIZE_RESOURCES_INFORMATION, HEAP_OPTIMIZE_RESOURCES_INFORMATION structure, PHEAP_OPTIMIZE_RESOURCES_INFORMATION, PHEAP_OPTIMIZE_RESOURCES_INFORMATION structure pointer, _HEAP_OPTIMIZE_RESOURCES_INFORMATION, base.heap_optimize_resources_information, winnt/HEAP_OPTIMIZE_RESOURCES_INFORMATION, winnt/PHEAP_OPTIMIZE_RESOURCES_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: HEAP_OPTIMIZE_RESOURCES_INFORMATION, *PHEAP_OPTIMIZE_RESOURCES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - HEAP_OPTIMIZE_RESOURCES_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _HEAP_OPTIMIZE_RESOURCES_INFORMATION structure


## -description


Specifies  flags for a HeapOptimizeResources operation initiated with <a href="https://msdn.microsoft.com/33c262ca-5093-4f44-a8c6-09045bc90f60">HeapSetInformation</a>.


## -struct-fields




### -field Version


### -field Flags


## -remarks



Mandatory parameter to the HeapOptimizeResources class.

The <b>HEAP_OPTIMIZE_RESOURCES_CURRENT_VERSION</b> constant is available to fill in the Version field of the <b>HEAP_OPTIMIZE_RESOURCES_INFORMATION</b> structure. The only legal value for this field is currently 1. 




## -see-also




<a href="https://msdn.microsoft.com/02a2a874-9ced-4b7d-8aad-4a7768639a32">Memory Management Structures</a>



<a href="https://msdn.microsoft.com/a7aeeb66-afd0-4871-81a3-e4619ac84293">PrefetchVirtualMemory</a>
 

 

