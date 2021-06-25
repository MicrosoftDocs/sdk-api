---
UID: NS:presentation.IPresentStatusPresentStatisticsVtbl
tech.root: composition_presentation
title: IPresentStatusPresentStatisticsVtbl
ms.date: 06/08/2021
targetos: Windows
description: 
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: presentation.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: IPresentStatusPresentStatisticsVtbl
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - IPresentStatusPresentStatisticsVtbl
f1_keywords:
 - IPresentStatusPresentStatisticsVtbl
 - presentation/IPresentStatusPresentStatisticsVtbl
dev_langs:
 - c++
---

## -description

Represents a v-table of pointers to `IPresentStatusPresentStatistics` functions.

## -struct-fields

### -field b

### -field QueryInterface

Queries a COM object for a pointer to one of its interfaces.

### -field AddRef

Increments the reference count for an interface pointer to a COM object.

### -field Release

Decrements the reference count for an interface on a COM object.

### -field GetPresentId

Gets the identifier of the present to which this statistic corresponds.

### -field GetKind

Gets the specific kind of present statistics to which this data corresponds.

### -field GetCompositionFrameId

Gets the ID of the composition frame on which the present was processed, skipped, or canceled.

### -field GetPresentStatus

Gets the status of the frame.

## -remarks

## -see-also

[IPresentStatusPresentStatistics](nn-presentation-ipresentstatuspresentstatistics.md), [IUnknown interface](/windows/win32/api/unknwn/nn-unknwn-iunknown)
