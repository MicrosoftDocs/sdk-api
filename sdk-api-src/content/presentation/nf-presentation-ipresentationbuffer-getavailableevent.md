---
UID: NF:presentation.IPresentationBuffer.GetAvailableEvent
tech.root: comp_swapchain
title: IPresentationBuffer::GetAvailableEvent
ms.date: 06/08/2021
targetos: Windows
description: Gets a handle to an event that signals when the buffer is available.
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
 - IPresentationBuffer::GetAvailableEvent
f1_keywords:
 - IPresentationBuffer::GetAvailableEvent
 - presentation/IPresentationBuffer::GetAvailableEvent
dev_langs:
 - c++
---

## -description

Gets a handle to an event that signals when the buffer is available.

## -parameters

### -param availableEventHandle

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to the event.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

The caller is responsible for closing the returned event.

An application can wait on and query this event, but it cannot modify its state. The presentation manager controls this event.

## -see-also

