---
UID: NF:presentation.ICompositionFramePresentStatistics.GetDisplayInstanceArray
tech.root: comp_swapchain
title: ICompositionFramePresentStatistics::GetDisplayInstanceArray
ms.date: 06/08/2021
targetos: Windows
description: Gets the array of display instances and its count.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dcomp.dll
req.header: presentation.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dcomp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - presentation.h
api_name:
 - ICompositionFramePresentStatistics::GetDisplayInstanceArray
f1_keywords:
 - ICompositionFramePresentStatistics::GetDisplayInstanceArray
 - presentation/ICompositionFramePresentStatistics::GetDisplayInstanceArray
dev_langs:
 - c++
---

## -description

Gets the array of display instances and its count.

## -parameters

### -param displayInstanceArrayCount

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The count of the _`displayInstanceArray`_.

### -param displayInstanceArray

Type: **[CompositionFrameDisplayInstance](ns-presentation-compositionframedisplayinstance.md) \*\***

The array of display instances.

## -remarks

This data is valid for the lifetime of the `ICompositionFramePresentStatistics`, and should not be read after the `ICompositionFramePresentStatistics` is released.

## -see-also

