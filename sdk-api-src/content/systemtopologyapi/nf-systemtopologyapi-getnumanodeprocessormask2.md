---
UID: NF:systemtopologyapi.GetNumaNodeProcessorMask2
tech.root: ProcThread
title: GetNumaNodeProcessorMask2
ms.date: 03/12/2021
ms.topic: language-reference
targetos: Windows
description: Retrieves the multi-group processor mask of the specified node.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: systemtopologyapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-systemtopology-l1-1-2.dll
 - systemtopologyapi.h
api_name:
 - GetNumaNodeProcessorMask2
f1_keywords:
 - GetNumaNodeProcessorMask2
 - systemtopologyapi/GetNumaNodeProcessorMask2
dev_langs:
 - c++
---

## -description

Retrieves the multi-group processor mask of the specified node.

## -parameters

### -param NodeNumber

Supplies the zero-based node number for the node of interest.

### -param ProcessorMasks

An array of [GROUP_AFFINITY](../winnt/ns-winnt-group_affinity.md) structures, which upon successful return describes the processor mask of the specified node.

Each element in the array describes a set of processors that belong to the node within a single processor group. There will be one element in the resulting array for each processor group this node has active processors in.


### -param ProcessorMaskCount

Specifies the size of the *ProcessorMasks* array, in elements.

### -param RequiredMaskCount

On successful return, specifies the number of affinity structures written to the array.

If the input array was too small, the function fails with **ERROR_INSUFFICIENT_BUFFER** and sets the *RequiredMaskCount* parameter to the number of elements required. 

The number of required elements is always less than or equal to the maximum group count returned by [GetMaximumProcessorGroupCount](../winbase/nf-winbase-getmaximumprocessorgroupcount.md).


## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero and extended error information can be retrieved by calling [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

If the array supplied is too small, the error value is **ERROR_INSUFFICIENT_BUFFER** and the RequiredMaskCount parameter is set to the number of elements required.

If the *NodeNumber* supplied is invalid (i.e. greater than the value returned by GetNumaHighestNodeNumber), the error value is **ERROR_INVALID_PARAMETER**.


## -remarks

If the node specified does not have any processors associated with it (i.e. it only contains memory or peripherals), then the *RequiredMaskCount* returned will be 0 and no structures will be written to the array.

## -see-also

[GetMaximumProcessorGroupCount](../winbase/nf-winbase-getmaximumprocessorgroupcount.md)
