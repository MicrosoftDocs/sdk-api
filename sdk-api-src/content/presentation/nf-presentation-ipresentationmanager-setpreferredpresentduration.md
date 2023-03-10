---
UID: NF:presentation.IPresentationManager.SetPreferredPresentDuration
tech.root: comp_swapchain
title: IPresentationManager::SetPreferredPresentDuration
ms.date: 06/08/2021
targetos: Windows
description: Sets the preferred frame duration.
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
 - IPresentationManager::SetPreferredPresentDuration
f1_keywords:
 - IPresentationManager::SetPreferredPresentDuration
 - presentation/IPresentationManager::SetPreferredPresentDuration
dev_langs:
 - c++
---

## -description

Sets the preferred frame duration.

## -parameters

### -param preferredDuration

Type: **[SystemInterruptTime](../presentationtypes/ns-presentationtypes-systeminterrupttime.md)**

The requested duration, in interrupt time.

### -param deviationTolerance

Type: **[SystemInterruptTime](../presentationtypes/ns-presentationtypes-systeminterrupttime.md)**

The allowed tolerance. If the magnitude of the difference between a supported system duration and the _`preferredDuration`_ parameter is within the _`deviationTolerance`_ parameter, that system duration will be used.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

Preferred frame duration is meant to be used as a hint to the system that it would be preferred to refresh the output at the specified framerate. Displays that support this rate, or a multiple, will be set into that mode if appropriate.

This parameter setting persists across presents.

## -see-also

