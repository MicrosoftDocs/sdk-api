---
UID: NF:presentation.IPresentationManager.ForceVSyncInterrupt
tech.root: comp_swapchain
title: IPresentationManager::ForceVSyncInterrupt
ms.date: 06/08/2021
targetos: Windows
description: Sets a value that indicates whether the GPU should always issue a VSync interrupt when a present is shown.
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
 - IPresentationManager::ForceVSyncInterrupt
f1_keywords:
 - IPresentationManager::ForceVSyncInterrupt
 - presentation/IPresentationManager::ForceVSyncInterrupt
dev_langs:
 - c++
---

## -description

Sets a value that indicates whether the GPU should always issue a VSync interrupt when a present is shown.

## -parameters

### -param forceVsyncInterrupt

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

`TRUE` to always issue a VSync interrupt; otherwise, `FALSE`.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

In order to take advantage of systems with hardware flip queue support, presents can be handled completely by the GPU without CPU involvement. This has power-saving benefits, but also means that buffer available events, the present retiring fence, and present statistics may not update immediately when the present is shown, but instead may update quite a bit later when the GPU periodically updates the CPU regarding what it has done independently.

An application can allow certain presents it doesn't need immediate feedback about to participate in this behavior by explicitly controlling whether the GPU should issue a VSync interrupt when each is shown. If not, such presents will result in improved power efficiency, at the cost of delayed feedback.

By default, presents will always force a VSync interrupt. Applications can opt into allowing some presents to not force a VSync interrupt by calling this method. If a system does not offer hardware flip queue support, all presents will issue a VSync interrupt and update the CPU, regardless of this setting.

This parameter setting persists across presents.

## -see-also

