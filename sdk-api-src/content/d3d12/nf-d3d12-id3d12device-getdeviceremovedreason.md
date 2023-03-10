---
UID: NF:d3d12.ID3D12Device.GetDeviceRemovedReason
title: ID3D12Device::GetDeviceRemovedReason (d3d12.h)
description: Gets the reason that the device was removed.
helpviewer_keywords: ["GetDeviceRemovedReason","GetDeviceRemovedReason method","GetDeviceRemovedReason method","ID3D12Device interface","ID3D12Device interface","GetDeviceRemovedReason method","ID3D12Device.GetDeviceRemovedReason","ID3D12Device::GetDeviceRemovedReason","d3d12/ID3D12Device::GetDeviceRemovedReason","direct3d12.id3d12device_getdeviceremovedreason"]
old-location: direct3d12\id3d12device_getdeviceremovedreason.htm
tech.root: direct3d12
ms.assetid: DA723656-BE64-474E-833B-D97576DE0449
ms.date: 12/05/2018
ms.keywords: GetDeviceRemovedReason, GetDeviceRemovedReason method, GetDeviceRemovedReason method,ID3D12Device interface, ID3D12Device interface,GetDeviceRemovedReason method, ID3D12Device.GetDeviceRemovedReason, ID3D12Device::GetDeviceRemovedReason, d3d12/ID3D12Device::GetDeviceRemovedReason, direct3d12.id3d12device_getdeviceremovedreason
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::GetDeviceRemovedReason
 - d3d12/ID3D12Device::GetDeviceRemovedReason
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.GetDeviceRemovedReason
---

## -description

Gets the reason that the device was removed, or **S_OK** if the device isn't removed. To be called back when a device is removed, consider using [ID3D12Fence::SetEventOnCompletion](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) with a value of **UINT64_MAX**. That's because device removal causes all fences to be signaled to that value (which also implies completing all events waited on, because they'll all be less than **UINT64_MAX**).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns the reason that the device was removed.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
