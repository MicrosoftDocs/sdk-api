---
UID: NS:comsvcs._ComponentStatistics
title: ComponentStatistics (comsvcs.h)
description: Represents statistical information about a COM+ component hosted in a particular process.
helpviewer_keywords: ["ComponentStatistics","ComponentStatistics structure [COM+]","comsvcs/ComponentStatistics","cos.componentstatistics"]
old-location: cos\componentstatistics.htm
tech.root: cos
ms.assetid: 26bc5fc4-3e34-41cc-ba11-5c13cf54521f
ms.date: 12/05/2018
ms.keywords: ComponentStatistics, ComponentStatistics structure [COM+], comsvcs/ComponentStatistics, cos.componentstatistics
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: ComponentStatistics
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ComponentStatistics
 - comsvcs/_ComponentStatistics
 - ComponentStatistics
 - comsvcs/ComponentStatistics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - ComponentStatistics
---

# ComponentStatistics structure


## -description

Represents statistical information about a COM+ component hosted in a particular process.

## -struct-fields

### -field NumInstances

The number of instances of the component in the hosting process.

### -field NumBoundReferences

The number of client references bound to an instance of this component.

### -field NumPooledObjects

The number of instances of the component in the hosting process's object pool.

### -field NumObjectsInCall

The number of instances of the component that are currently servicing a call.

### -field AvgResponseTimeInMs

A rolling average of the time it takes an instance of this component to service a call.

### -field NumCallsCompletedRecent

The number of calls to instances of this component that have completed (successfully or not) in a recent time period (for comparison with <b>NumCallsFailedRecent</b>).

### -field NumCallsFailedRecent

The number of calls to instances of this component that have failed in a recent time period (for comparison with <b>NumCallsCompletedRecent</b>).

### -field NumCallsCompletedTotal

The total number of calls to instances of this component that have completed (successfully or not) throughout the lifetime of the hosting process. This data is not currently available, and this member is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field NumCallsFailedTotal

The total number of calls to instances of this component that have failed throughout the lifetime of the hosting process. This data is not currently available, and this member is always set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field Reserved1

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field Reserved2

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field Reserved3

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

### -field Reserved4

This member is reserved and set to DATA_NOT_AVAILABLE (0xFFFFFFFF).

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetapptrackerdata">IGetAppTrackerData</a>