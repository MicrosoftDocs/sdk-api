---
UID: NF:presentation.IPresentationManager.GetNextPresentStatistics
tech.root: comp_swapchain
title: IPresentationManager::GetNextPresentStatistics
ms.date: 06/08/2021
targetos: Windows
description: Gets the next present statistics item in the queue.
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
 - IPresentationManager::GetNextPresentStatistics
f1_keywords:
 - IPresentationManager::GetNextPresentStatistics
 - presentation/IPresentationManager::GetNextPresentStatistics
dev_langs:
 - c++
---

## -description

Gets the next present statistics item in the queue.

## -parameters

### -param nextPresentStatistics

Type: **[IPresentStatistics](nn-presentation-ipresentstatistics.md) \*\***

A pointer to the next present statistics item in the queue , or `nullptr` if the queue is empty.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

If the present statistics queue is empty, no error will be returned. Instead, `nullptr` will be returned in the out parameter.

## -see-also

