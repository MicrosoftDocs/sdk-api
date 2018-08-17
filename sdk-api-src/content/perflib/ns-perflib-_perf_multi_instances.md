---
UID: NS:perflib._PERF_MULTI_INSTANCES
title: "_PERF_MULTI_INSTANCES"
author: windows-sdk-content
description: Provides information about the PERF_MULTI_INSTANCES block that contains the structure.
old-location: perf\perf_multi_instances.htm
old-project: perfctrs
ms.assetid: 5EC34ECD-D240-4B44-A52B-C5518918400C
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PPERF_MULTI_INSTANCES, PERF_MULTI_INSTANCES, PERF_MULTI_INSTANCES structure [Perf], PPERF_MULTI_INSTANCES, PPERF_MULTI_INSTANCES structure pointer [Perf], _PERF_MULTI_INSTANCES, perf.perf_multi_instances, perflib/PERF_MULTI_INSTANCES, perflib/PPERF_MULTI_INSTANCES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: perflib.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PERF_MULTI_INSTANCES, *PPERF_MULTI_INSTANCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_MULTI_INSTANCES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PERF_MULTI_INSTANCES structure


## -description


Provides information about the <b>PERF_MULTI_INSTANCES</b> block that contains the structure. A <b>PERF_MULTI_INSTANCES</b> block indicates the number of instances for which results are provided as part of the <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> block in multiple-instance query. The <b>PERF_MULTI_INSTANCES</b> block consists of the following items in order:<ol>
<li>A <b>PERF_MULTI_INSTANCES</b> structure</li>
<li>A number of instance data blocks. The number of instance data blocks that the <b>PERF_MULTI_INSTANCES</b> block contains is indicated ny the <b>dwInstances</b> member of the <b>PERF_MULTI_INSTANCES</b> structure. Each instance data block
consists of the following items in order:<ol>
<li>A <a href="https://msdn.microsoft.com/58E4062A-0CE4-4FF7-A9B2-CA0947563C7B">PERF_INSTANCE_HEADER</a> block</li>
<li>A number of
<a href="https://msdn.microsoft.com/19D65E98-182E-45CC-946F-F1924CB78029">PERF_COUNTER_DATA</a> blocks. The number of <b>PERF_COUNTER_DATA</b> blocks depends on
the context:<ul>
<li>If the <b>PERF_MULTI_INSTANCES</b> block is part of a
<a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> block with type <b>PERF_MULTIPLE_INSTANCES</b>, the instance data block contains one
<a href="https://msdn.microsoft.com/19D65E98-182E-45CC-946F-F1924CB78029">PERF_COUNTER_DATA</a> block.</li>
<li> If the <b>PERF_MULTI_INSTANCES</b> block is part of a
<a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> block with type <b>PERF_COUNTERSET</b>, the number of
<a href="https://msdn.microsoft.com/19D65E98-182E-45CC-946F-F1924CB78029">PERF_COUNTER_DATA</a> blocks is indicated by the <a href="https://msdn.microsoft.com/4F490C3C-F587-4E7B-B316-162EDA76EC30">PERF_MULTI_COUNTERS</a> block.</li>
</ul>
</li>
</ol>
</li>
</ol>



## -struct-fields




### -field dwTotalSize

The total size of the <b>PERF_MULTI_INSTANCES</b> block, in bytes. This total size is the sum of the sizes of the <b>PERF_MULTI_INSTANCES</b> structure and the instance data blocks.


### -field dwInstances

The number of instance data blocks in the <b>PERF_MULTI_INSTANCES</b> block.


## -remarks



The <a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a> function gets a <a href="https://msdn.microsoft.com/0B30B30A-2B2D-43D8-B6DD-58C70D54EB58">PERF_DATA_HEADER</a> block that may
contain <b>PERF_MULTI_INSTANCES</b> blocks within the <a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a> block.




## -see-also




<a href="https://msdn.microsoft.com/8C07E4BB-61CD-4A0F-8C23-86BE7DAA415F">PERF_COUNTER_HEADER</a>



<a href="https://msdn.microsoft.com/0B30B30A-2B2D-43D8-B6DD-58C70D54EB58">PERF_DATA_HEADER</a>



<a href="https://msdn.microsoft.com/EBCF00E0-6C40-40E5-9F3D-9AE5F9AB74AC">PerfQueryCounterData</a>
 

 

