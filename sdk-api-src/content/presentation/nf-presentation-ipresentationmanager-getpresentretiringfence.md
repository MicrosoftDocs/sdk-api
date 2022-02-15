---
UID: NF:presentation.IPresentationManager.GetPresentRetiringFence
tech.root: comp_swapchain
title: IPresentationManager::GetPresentRetiringFence
ms.date: 06/08/2021
targetos: Windows
description: Gets a fence that signals when a present is retiring.
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
 - IPresentationManager::GetPresentRetiringFence
f1_keywords:
 - IPresentationManager::GetPresentRetiringFence
 - presentation/IPresentationManager::GetPresentRetiringFence
dev_langs:
 - c++
---

## -description

Gets a fence that signals when a present is retiring.

## -parameters

### -param riid

Type: **REFIID**

A reference to the interface identifier (IID) of the interface being queried for.

### -param fence

Type: **[void](/windows/desktop/winprog/windows-data-types)\*\***

The address of a pointer to an interface with the IID specified in the _`riid`_ parameter.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

This fence will be signaled to the Present ID of each present when that present has begun retiring - that is, a subsequent present has been queued to take its place.

## -see-also

