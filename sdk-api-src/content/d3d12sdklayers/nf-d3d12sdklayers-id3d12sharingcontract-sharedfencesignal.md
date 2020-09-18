---
UID: NF:d3d12sdklayers.ID3D12SharingContract.SharedFenceSignal
title: ID3D12SharingContract::SharedFenceSignal (d3d12sdklayers.h)
description: Signals a shared fence between the D3D layers and diagnostics tools.
helpviewer_keywords: ["ID3D12SharingContract interface","SharedFenceSignal method","ID3D12SharingContract.SharedFenceSignal","ID3D12SharingContract::SharedFenceSignal","SharedFenceSignal","SharedFenceSignal method","SharedFenceSignal method","ID3D12SharingContract interface","d3d12sdklayers/ID3D12SharingContract::SharedFenceSignal","direct3d12.id3d12sharingcontract_sharedfencesignal"]
old-location: direct3d12\id3d12sharingcontract_sharedfencesignal.htm
tech.root: direct3d12
ms.assetid: E90576A7-B665-4911-A17E-FD328CD71458
ms.date: 12/05/2018
ms.keywords: ID3D12SharingContract interface,SharedFenceSignal method, ID3D12SharingContract.SharedFenceSignal, ID3D12SharingContract::SharedFenceSignal, SharedFenceSignal, SharedFenceSignal method, SharedFenceSignal method,ID3D12SharingContract interface, d3d12sdklayers/ID3D12SharingContract::SharedFenceSignal, direct3d12.id3d12sharingcontract_sharedfencesignal
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12SharingContract::SharedFenceSignal
 - d3d12sdklayers/ID3D12SharingContract::SharedFenceSignal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12SharingContract.SharedFenceSignal
---

# ID3D12SharingContract::SharedFenceSignal


## -description

Signals a shared fence between the D3D layers and diagnostics tools.

## -parameters

### -param pFence [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>*</b>

A pointer to the shared fence to signal.

### -param FenceValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

An unsigned 64bit value to signal the shared fence with.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract">ID3D12SharingContract</a>