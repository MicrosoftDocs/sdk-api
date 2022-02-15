---
UID: NF:presentation.IPresentationManager.AddBufferFromSharedHandle
tech.root: comp_swapchain
title: IPresentationManager::AddBufferFromSharedHandle
ms.date: 06/08/2021
targetos: Windows
description: Adds a shared DXGI resource to the presentation manager to be tracked as a presentation buffer.
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IPresentationManager::AddBufferFromSharedHandle
f1_keywords:
 - IPresentationManager::AddBufferFromSharedHandle
 - presentation/IPresentationManager::AddBufferFromSharedHandle
dev_langs:
 - c++
---

## -description

Adds a shared DXGI resource to the presentation manager to be tracked as a presentation buffer.

## -parameters

### -param dxgiSharedResourceHandle

Type: **[HANDLE](/windows/desktop/winprog/windows-data-types)**

The handle to a shared DXGI resource.

### -param presentationBuffer

Type: **[IPresentationBuffer](nn-presentation-ipresentationbuffer.md)**

The returned presentation buffer that references the DXGI resource.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

