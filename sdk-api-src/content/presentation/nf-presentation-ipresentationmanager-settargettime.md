---
UID: NF:presentation.IPresentationManager.SetTargetTime
tech.root: comp_swapchain
title: IPresentationManager::SetTargetTime
ms.date: 06/08/2021
targetos: Windows
description: Sets a target time for the next present.
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
 - IPresentationManager::SetTargetTime
f1_keywords:
 - IPresentationManager::SetTargetTime
 - presentation/IPresentationManager::SetTargetTime
dev_langs:
 - c++
---

## -description

Sets a target time for the next present.

## -parameters

### -param targetTime

Type: **[SystemInterruptTime](../presentationtypes/ns-presentationtypes-systeminterrupttime.md)**

The target time for the next present.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

The system will attempt to display the present as close to the specified time as possible.

This parameter setting persists across presents.

## -see-also

