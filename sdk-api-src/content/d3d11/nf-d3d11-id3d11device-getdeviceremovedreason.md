---
UID: NF:d3d11.ID3D11Device.GetDeviceRemovedReason
title: ID3D11Device::GetDeviceRemovedReason (d3d11.h)
description: Get the reason why the device was removed. (ID3D11Device.GetDeviceRemovedReason)
helpviewer_keywords: ["09615373-9ecd-296a-1d5f-ef9f2b085826","GetDeviceRemovedReason","GetDeviceRemovedReason method [Direct3D 11]","GetDeviceRemovedReason method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","GetDeviceRemovedReason method","ID3D11Device.GetDeviceRemovedReason","ID3D11Device::GetDeviceRemovedReason","d3d11/ID3D11Device::GetDeviceRemovedReason","direct3d11.id3d11device_getdeviceremovedreason"]
old-location: direct3d11\id3d11device_getdeviceremovedreason.htm
tech.root: direct3d11
ms.assetid: 9e09c954-5c61-49fd-b25a-87dc0051a84d
ms.date: 12/05/2018
ms.keywords: 09615373-9ecd-296a-1d5f-ef9f2b085826, GetDeviceRemovedReason, GetDeviceRemovedReason method [Direct3D 11], GetDeviceRemovedReason method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],GetDeviceRemovedReason method, ID3D11Device.GetDeviceRemovedReason, ID3D11Device::GetDeviceRemovedReason, d3d11/ID3D11Device::GetDeviceRemovedReason, direct3d11.id3d11device_getdeviceremovedreason
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::GetDeviceRemovedReason
 - d3d11/ID3D11Device::GetDeviceRemovedReason
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device.GetDeviceRemovedReason
---

# ID3D11Device::GetDeviceRemovedReason


## -description

Get the reason why the device was removed.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: 



<ul>
<li>DXGI_ERROR_DEVICE_HUNG</li>
<li>DXGI_ERROR_DEVICE_REMOVED</li>
<li>DXGI_ERROR_DEVICE_RESET</li>
<li>DXGI_ERROR_DRIVER_INTERNAL_ERROR</li>
<li>DXGI_ERROR_INVALID_CALL</li>
<li>S_OK</li>
</ul>
For more detail on these return codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
