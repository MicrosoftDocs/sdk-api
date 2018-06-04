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
 

 

