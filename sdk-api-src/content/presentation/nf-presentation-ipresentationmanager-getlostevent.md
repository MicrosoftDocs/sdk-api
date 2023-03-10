---
UID: NF:presentation.IPresentationManager.GetLostEvent
tech.root: comp_swapchain
title: IPresentationManager::GetLostEvent
ms.date: 06/08/2021
targetos: Windows
description: Gets a handle to an event that signals when the presentation manager hits an error it cannot recover from.
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
 - IPresentationManager::GetLostEvent
f1_keywords:
 - IPresentationManager::GetLostEvent
 - presentation/IPresentationManager::GetLostEvent
dev_langs:
 - c++
---

## -description

Gets a handle to an event that signals when the presentation manager hits an error it cannot recover from.

## -parameters

### -param lostEventHandle

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**

A handle to the event.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

The returned event will be signaled when the presentation manager hits an error it cannot recover from. In this case, the application should release this presentation manager and create a new one.

An application can wait on and query this event, but it cannot modify its state. The presentation manager controls this event.

## -see-also

