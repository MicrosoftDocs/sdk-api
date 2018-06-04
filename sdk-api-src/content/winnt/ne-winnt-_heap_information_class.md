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

# _HEAP_INFORMATION_CLASS enumeration


## -description


Specifies the class of heap information to be set or retrieved. 


## -enum-fields




### -field HeapCompatibilityInformation

The heap features that are enabled. The available features vary based on operating system. Depending on the <i>HeapInformation</i> parameter in the <a href="https://msdn.microsoft.com/6bf6cb8b-7212-4ddb-9ea6-34bc78824a8f">HeapQueryInformation</a> or <a href="https://msdn.microsoft.com/33c262ca-5093-4f44-a8c6-09045bc90f60">HeapSetInformation</a> functions, specifying this enumeration value can indicate one of the following features:

<ul>
<li>A standard heap that does not support look-aside lists.</li>
<li>A heap that supports look-aside lists.</li>
<li>A <a href="https://msdn.microsoft.com/d10abf82-423c-4942-b05e-55de3a5c4219">low-fragmentation heap</a> (LFH), which does not support look-aside lists.</li>
</ul>
For more information about look-aside lists, see the Remarks section.


### -field HeapEnableTerminationOnCorruption

The terminate-on-corruption feature. If the heap manager detects an error in any heap used by the 
         process, it calls the Windows Error Reporting service and terminates the process.

After a process enables this feature, it cannot be disabled.


### -field HeapOptimizeResources




## -remarks



To retrieve information about a heap, use the <a href="https://msdn.microsoft.com/6bf6cb8b-7212-4ddb-9ea6-34bc78824a8f">HeapQueryInformation</a> function. To enable features for a heap, use the 
<a href="https://msdn.microsoft.com/33c262ca-5093-4f44-a8c6-09045bc90f60">HeapSetInformation</a> function.

<b>Windows XP and Windows Server 2003:  </b> A look-aside list is a fast memory allocation mechanism that contains only fixed-sized blocks. Look-aside lists are enabled by default for heaps that support them. Starting with Windows Vista, look-aside lists are not used and the LFH is enabled by default.

Look-aside lists are faster than general pool allocations that vary in size, because the system does not search for free memory that fits the allocation. In addition, access to look-aside lists is generally synchronized using fast atomic processor exchange instructions instead of mutexes or spinlocks. Look-aside lists can be created by the system or drivers. They can be allocated from paged or nonpaged pool. 








## -see-also




<a href="https://msdn.microsoft.com/6bf6cb8b-7212-4ddb-9ea6-34bc78824a8f">HeapQueryInformation</a>



<a href="https://msdn.microsoft.com/33c262ca-5093-4f44-a8c6-09045bc90f60">HeapSetInformation</a>
 

 

