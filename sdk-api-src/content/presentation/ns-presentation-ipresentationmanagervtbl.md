---
UID: NS:presentation.IPresentationManagerVtbl
tech.root: composition_presentation
title: IPresentationManagerVtbl
ms.date: 06/08/2021
targetos: Windows
description: Represents a v-table of pointers to `IPresentationManager` functions.
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
req.typenames: IPresentationManagerVtbl
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentation.h
api_name:
 - IPresentationManagerVtbl
f1_keywords:
 - IPresentationManagerVtbl
 - presentation/IPresentationManagerVtbl
dev_langs:
 - c++
---

## -description

Represents a v-table of pointers to `IPresentationManager` functions.

## -struct-fields

### -field b

### -field QueryInterface

Queries a COM object for a pointer to one of its interfaces.

### -field AddRef

Increments the reference count for an interface pointer to a COM object.

### -field Release

Decrements the reference count for an interface on a COM object.

### -field AddBufferFromSharedHandle

Adds a shared DXGI resource to the presentation manager to be tracked as a presentation buffer.

### -field CreatePresentationSurface

Creates a presentation surface for a piece of content that can be hosted in a visual tree and assigned a single front buffer.

### -field GetNextPresentId

Gets the identifier for the next present. All synchronization fences will be signaled to this value when referring to that present.

### -field SetTargetTime

Sets a target time for the next present.

### -field SetPreferredPresentDuration

Sets the preferred frame duration.

### -field ForceVSyncInterrupt

Sets a value that indicates whether the GPU should always issue a VSync interrupt when a present is shown.

### -field Present

Presents this presentation manager.

### -field GetPresentRetiringFence

Gets a fence that signals when a present is retiring.

### -field CancelPresentsFrom

Cancels any previously issued and still in-flight presents that have not yet displayed, and whose Present IDs are at least the passed in _`presentIdToCancelFrom`_.

### -field GetLostEvent

Gets a handle to an event that signals when the presentation manager hits an error it cannot recover from.

### -field GetPresentStatisticsAvailableEvent

Gets a handle to an event that signals when present statistics are available to report.

### -field EnablePresentStatisticsKind

Enables or disables the specified present statistics kind.

### -field GetNextPresentStatistics

Gets the next present statistics item in the queue.

## -remarks

## -see-also

[IPresentationManager](nn-presentation-ipresentationmanager.md), [IUnknown interface](/windows/win32/api/unknwn/nn-unknwn-iunknown)
