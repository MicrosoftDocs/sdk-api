---
UID: NS:perflib._PERF_COUNTERSET_INSTANCE
title: PERF_COUNTERSET_INSTANCE (perflib.h)
description: Defines an instance of a counter set.
helpviewer_keywords: ["*PPERF_COUNTERSET_INSTANCE","PERF_COUNTERSET_INSTANCE","PERF_COUNTERSET_INSTANCE structure [Perf]","PERF_COUNTERSET_INSTANCE","*PPERF_COUNTERSET_INSTANCE","PERF_COUNTERSET_INSTANCE","*PPERF_COUNTERSET_INSTANCE structure [Perf]","base.perf_counterset_instance","perf.perf_counterset_instance","perflib/PERF_COUNTERSET_INSTANCE"]
old-location: perf\perf_counterset_instance.htm
tech.root: perf
ms.assetid: 709d5339-cedd-4b03-9d8e-c125eb3bcac0
ms.date: 12/05/2018
ms.keywords: '*PPERF_COUNTERSET_INSTANCE, PERF_COUNTERSET_INSTANCE, PERF_COUNTERSET_INSTANCE structure [Perf], PERF_COUNTERSET_INSTANCE,*PPERF_COUNTERSET_INSTANCE, PERF_COUNTERSET_INSTANCE,*PPERF_COUNTERSET_INSTANCE structure [Perf], base.perf_counterset_instance, perf.perf_counterset_instance, perflib/PERF_COUNTERSET_INSTANCE'
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PERF_COUNTERSET_INSTANCE, *PPERF_COUNTERSET_INSTANCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PERF_COUNTERSET_INSTANCE
 - perflib/_PERF_COUNTERSET_INSTANCE
 - PPERF_COUNTERSET_INSTANCE
 - perflib/PPERF_COUNTERSET_INSTANCE
 - PERF_COUNTERSET_INSTANCE
 - perflib/PERF_COUNTERSET_INSTANCE
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
 - PERF_COUNTERSET_INSTANCE, *PPERF_COUNTERSET_INSTANCE
---

# PERF_COUNTERSET_INSTANCE structure


## -description

Defines an instance of a counter set.

## -struct-fields

### -field CounterSetGuid

GUID that identifies the counter set to which this instance belongs.

### -field dwSize

Size, in bytes, of the instance block. The instance block contains this structure, followed by one or more <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> blocks, and ends with the instance name.

### -field InstanceId

Identifier that uniquely identifies this instance. 

The provider specified the identifier when calling <a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a>.

### -field InstanceNameOffset

Byte offset from the beginning of this structure to the null-terminated Unicode instance name.

The provider specified the instance name when calling <a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a>.

### -field InstanceNameSize

Size, in bytes, of the instance name. The size includes the null-terminator.

## -remarks

The <b>Offset</b> member of  <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a> contains the byte offset from the beginning of the <b>PERF_COUNTERSET_INSTANCE</b> block to the counter's raw counter value.

## -see-also

<a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_info">PERF_COUNTER_INFO</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfcreateinstance">PerfCreateInstance</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfdeleteinstance">PerfDeleteInstance</a>



<a href="/windows/desktop/api/perflib/nf-perflib-perfqueryinstance">PerfQueryInstance</a>