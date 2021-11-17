---
UID: NF:presentation.IPresentationManager.Present
tech.root: comp_swapchain
title: IPresentationManager::Present
ms.date: 06/08/2021
targetos: Windows
description: Presents this presentation manager.
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
 - IPresentationManager::Present
f1_keywords:
 - IPresentationManager::Present
 - presentation/IPresentationManager::Present
dev_langs:
 - c++
---

## -description

Presents this presentation manager.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

If the presentation manager has become lost, this call will return `PRESENTATION_ERROR_LOST`. If the application receives that error, you must destroy this presentation manager and create a new one.

## -see-also

