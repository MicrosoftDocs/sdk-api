---
UID: NF:d3d12.ID3D12Device1.SetEventOnMultipleFenceCompletion
title: ID3D12Device1::SetEventOnMultipleFenceCompletion (d3d12.h)
description: Specifies an event that should be fired when one or more of a collection of fences reach specific values.
helpviewer_keywords: ["ID3D12Device1 interface","SetEventOnMultipleFenceCompletion method","ID3D12Device1.SetEventOnMultipleFenceCompletion","ID3D12Device1::SetEventOnMultipleFenceCompletion","SetEventOnMultipleFenceCompletion","SetEventOnMultipleFenceCompletion method","SetEventOnMultipleFenceCompletion method","ID3D12Device1 interface","d3d12/ID3D12Device1::SetEventOnMultipleFenceCompletion","direct3d12.id3d12device1_seteventonmultiplefencecompletion"]
old-location: direct3d12\id3d12device1_seteventonmultiplefencecompletion.htm
tech.root: direct3d12
ms.assetid: C187EEB7-DCD0-4535-AF0E-EF2C0E2DC83C
ms.date: 12/05/2018
ms.keywords: ID3D12Device1 interface,SetEventOnMultipleFenceCompletion method, ID3D12Device1.SetEventOnMultipleFenceCompletion, ID3D12Device1::SetEventOnMultipleFenceCompletion, SetEventOnMultipleFenceCompletion, SetEventOnMultipleFenceCompletion method, SetEventOnMultipleFenceCompletion method,ID3D12Device1 interface, d3d12/ID3D12Device1::SetEventOnMultipleFenceCompletion, direct3d12.id3d12device1_seteventonmultiplefencecompletion
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device1::SetEventOnMultipleFenceCompletion
 - d3d12/ID3D12Device1::SetEventOnMultipleFenceCompletion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Device1.SetEventOnMultipleFenceCompletion
---

## -description

Specifies an event that should be fired when one or more of a collection of fences reach specific values.

## -parameters

### -param ppFences [in]

Type: <b>ID3D12Fence*</b>

An array of length <i>NumFences</i> that specifies the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a> objects.

### -param pFenceValues [in]

Type: <b>const UINT64*</b>

An array of length <i>NumFences</i> that specifies the fence values required for the event is to be signaled.

### -param NumFences

Type: <b>UINT</b>

Specifies the number of fences to be included.

### -param Flags

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags">D3D12_MULTIPLE_FENCE_WAIT_FLAGS</a></b>

Specifies one  of the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_multiple_fence_wait_flags">D3D12_MULTIPLE_FENCE_WAIT_FLAGS</a> that determines how to proceed.

### -param hEvent

Type: <b>HANDLE</b>

A handle to the event object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -remarks

To specify a single fence refer to the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion">SetEventOnCompletion</a> method.

If *hEvent* is a null handle, then this API will not return until the specified fence value(s) have been reached.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>