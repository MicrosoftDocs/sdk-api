---
UID: NF:d3d12sdklayers.ID3D12Debug4.DisableDebugLayer
title: ID3D12Debug4::DisableDebugLayer
description: Disables the debug layer.
tech.root: direct3d12
ms.date: 07/26/2021
req.construct-type: function
req.header: d3d12sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - ID3D12Debug4::DisableDebugLayer
 - d3d12sdklayers/ID3D12Debug4::DisableDebugLayer
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug4::DisableDebugLayer
---

## -description

Disables the debug layer.

**DisableDebugLayer** takes effect only when all [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) objects (for a given adapter) have been released. See **Remarks** for [D3D12CreateDevice](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice).

## -remarks

## -see-also

* [ID3D12Debug4](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug4)
