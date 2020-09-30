---
UID: NS:perflib._PERF_INSTANCE_HEADER
title: PERF_INSTANCE_HEADER (perflib.h)
description: Provides information about the PERF_INSTANCE_HEADER block that contains the structure.
helpviewer_keywords: ["*PPERF_INSTANCE_HEADER","PERF_INSTANCE_HEADER","PERF_INSTANCE_HEADER structure [Perf]","PPERF_INSTANCE_HEADER","PPERF_INSTANCE_HEADER structure pointer [Perf]","perf.perf_instance_header","perflib/PERF_INSTANCE_HEADER","perflib/PPERF_INSTANCE_HEADER"]
old-location: perf\perf_instance_header.htm
tech.root: perf
ms.assetid: 58E4062A-0CE4-4FF7-A9B2-CA0947563C7B
ms.date: 12/05/2018
ms.keywords: '*PPERF_INSTANCE_HEADER, PERF_INSTANCE_HEADER, PERF_INSTANCE_HEADER structure [Perf], PPERF_INSTANCE_HEADER, PPERF_INSTANCE_HEADER structure pointer [Perf], perf.perf_instance_header, perflib/PERF_INSTANCE_HEADER, perflib/PPERF_INSTANCE_HEADER'
req.header: perflib.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PERF_INSTANCE_HEADER, *PPERF_INSTANCE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_INSTANCE_HEADER
 - perflib/_PERF_INSTANCE_HEADER
 - PPERF_INSTANCE_HEADER
 - perflib/PPERF_INSTANCE_HEADER
 - PERF_INSTANCE_HEADER
 - perflib/PERF_INSTANCE_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PERF_INSTANCE_HEADER
---

# PERF_INSTANCE_HEADER structure


## -description

Provides information about the <b>PERF_INSTANCE_HEADER</b> block that contains the structure. A <b>PERF_INSTANCE_HEADER</b> block provides information about the instances in a counter set, or the instances for which performance counter results are provided in a multiple-instance query. The  <b>PERF_INSTANCE_HEADER</b> block consists of the following items in order: <ol>
<li>A <b>PERF_INSTANCE_HEADER</b> structure
that contains the size of the <b>PERF_INSTANCE_HEADER</b> block and the instance identifier</li>
<li>A null-terminated UTF-16LE string that contains the instance name.</li>
<li>Padding such that the total size of the <b>PERF_INSTANCE_HEADER</b> block is a multiple of 8 bytes.
</li>
</ol>

## -struct-fields

### -field Size

The total size of the <b>PERF_INSTANCE_HEADER</b> block, in bytes. This total size is the sum of the sizes of the <b>PERF_INSTANCE_HEADER</b> structures, the string that  contains the instance name, and the padding.

### -field InstanceId

The instance identifier.

## -remarks

Each active instance of a counter set is identified by the combination of  

its instance name and instance identifier. Two active instances of a  

counter set should not have the same combination of instance name and instance  

identifier. Clients, however, should tolerate instances with duplicate combinations of instance name and instance  

identifier. 

The <a href="/windows/desktop/api/perflib/nf-perflib-perfenumeratecountersetinstances">PerfEnumerateCounterSetInstances</a> function gets a sequence of  

<b>PERF_INSTANCE_HEADER</b> blocks.  

  

The <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a> function gets a <a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a> block that may  

contain <b>PERF_INSTANCE_HEADER</b> blocks within the <a href="/windows/desktop/api/perflib/ns-perflib-perf_multi_instances">PERF_MULTI_INSTANCES</a> block.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_data_header">PERF_DATA_HEADER</a>



<a href="/windows/desktop/api/perflib/ns-perflib-perf_instance_header">PERF_INSTANCE_HEADER</a>



<a href="/windows/desktop/api/perflib/ns-perflib-perf_multi_instances">PERF_MULTI_INSTANCES</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfenumeratecountersetinstances">PerfEnumerateCounterSetInstances</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycounterdata">PerfQueryCounterData</a>