---
UID: NS:presentation.IIndependentFlipFramePresentStatisticsVtbl
tech.root: composition_presentation
title: IIndependentFlipFramePresentStatisticsVtbl
ms.date: 06/08/2021
targetos: Windows
description: Represents a v-table of pointers to `IIndependentFlipFramePresentStatistics` functions.
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
req.typenames: IIndependentFlipFramePresentStatisticsVtbl
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - IIndependentFlipFramePresentStatisticsVtbl
f1_keywords:
 - IIndependentFlipFramePresentStatisticsVtbl
 - presentation/IIndependentFlipFramePresentStatisticsVtbl
dev_langs:
 - c++
---

## -description

Represents a v-table of pointers to `IIndependentFlipFramePresentStatistics` functions.

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

### -field GetOutputAdapterLUID

Gets the locally unique ID (LUID) that refers to the display adapter on which this independent-flip present occurred.

### -field GetOutputVidPnSourceId

Gets an integer that identifies a video present source on the display adapter.

### -field GetContentTag

Gets the tag of the content on which statistics are being reporting.

### -field GetDisplayedTime

Gets the time the present was displayed.

### -field GetPresentDuration

Gets the actual amount of time the present was displayed.

## -remarks

## -see-also

[IIndependentFlipFramePresentStatistics](nn-presentation-iindependentflipframepresentstatistics.md), [IUnknown interface](/windows/win32/api/unknwn/nn-unknwn-iunknown)
