---
UID: NF:presentation.IPresentationManager.CancelPresentsFrom
tech.root: comp_swapchain
title: IPresentationManager::CancelPresentsFrom
ms.date: 06/08/2021
targetos: Windows
description: Cancels any previously issued and still in-flight presents that have not yet displayed, and whose Present IDs are at least the passed in _`presentIdToCancelFrom`_.
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
 - IPresentationManager::CancelPresentsFrom
f1_keywords:
 - IPresentationManager::CancelPresentsFrom
 - presentation/IPresentationManager::CancelPresentsFrom
dev_langs:
 - c++
---

## -description

Cancels any previously issued and still in-flight presents that have not yet displayed, and whose Present IDs are at least the passed in _`presentIdToCancelFrom`_.

## -parameters

### -param presentIdToCancelFrom

Type: **[UINT64](/windows/desktop/winprog/windows-data-types)**

The identifier of the present from which to cancel presents that have been issued but not yet displayed.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

If any presents in the past have already been displayed, this call will not fail - those presents will simply not be canceled. The present retiring fence will not be signaled for any canceled presents, because when presents are canceled, they don't affect the currently displayed present or cause it to begin the retiring process. For this reason, it is suggested that after performing a present, an application queries buffer available events to find an available buffer to issue on the first present after a cancel. Once that present is queued, it allows the previously displayed present to begin the retiring process, and signal the present retiring fence.

## -see-also

[IPresentationBuffer::GetAvailableEvent](nf-presentation-ipresentationbuffer-getavailableevent.md)
