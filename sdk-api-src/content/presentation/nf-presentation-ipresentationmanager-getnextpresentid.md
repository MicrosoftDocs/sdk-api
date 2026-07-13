---
UID: NF:presentation.IPresentationManager.GetNextPresentId
tech.root: comp_swapchain
title: IPresentationManager::GetNextPresentId
ms.date: 06/08/2021
targetos: Windows
description: Gets the identifier for the next present. All synchronization fences will be signaled to this value when referring to that present.
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
 - IPresentationManager::GetNextPresentId
f1_keywords:
 - IPresentationManager::GetNextPresentId
 - presentation/IPresentationManager::GetNextPresentId
dev_langs:
 - c++
---

## -description

Gets the identifier for the next present. All synchronization fences will be signaled to this value when referring to that present.

## -returns

Type: **[UINT64](/windows/desktop/winprog/windows-data-types)**

The identifier for the next present.

## -remarks

## -see-also

