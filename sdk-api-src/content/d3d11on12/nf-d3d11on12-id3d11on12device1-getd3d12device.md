---
UID: NF:d3d11on12.ID3D11On12Device1.GetD3D12Device
title: ID3D11On12Device1::GetD3D12Device (d3d11on12.h)
description: Retrieves the [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) being interoperated with.
tech.root: direct3d12
ms.date: 02/25/2019
ms.keywords: ID3D11On12Device1::GetD3D12Device
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: D3D11.dll
req.header: d3d11on12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: D3D11.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D11On12Device1::GetD3D12Device
 - d3d11on12/ID3D11On12Device1::GetD3D12Device
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d11on12.h
api_name:
 - ID3D11On12Device1::GetD3D12Device
---

## -description

Retrieves the [Direct3D 12 device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) being interoperated with. This enables better interoperability with a component that might be handed a Direct3D 11 device, but which wants to leverage Direct3D 12 instead.

## -parameters

### -param riid

Type: **REFIID**

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in `ppvDevice`. This is expected to be the GUID of [ID3D12Device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

### -param ppvDevice

Type: **[void](/windows/desktop/winprog/windows-data-types)\*\***

A pointer to a memory block that receives a pointer to the device. This is the address of a pointer to an [ID3D12Device](/windows/desktop/api/d3d12/nn-d3d12-id3d12device), representing the Direct3D 12 device.

## -returns

Type: **[HRESULT](/windows/desktop/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

## -see-also

* [ID3D12Device interface](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)

