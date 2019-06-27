---
UID: NF:d3d10.ID3D10Device.GetDeviceRemovedReason
title: ID3D10Device::GetDeviceRemovedReason (d3d10.h)
author: windows-sdk-content
description: Get the reason why the device was removed.
old-location: direct3d10\id3d10device_getdeviceremovedreason.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_getdeviceremovedreason.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0009e4c5-6ad8-a897-de23-d289a78f9671, GetDeviceRemovedReason, GetDeviceRemovedReason method [Direct3D 10], GetDeviceRemovedReason method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GetDeviceRemovedReason method, ID3D10Device.GetDeviceRemovedReason, ID3D10Device::GetDeviceRemovedReason, d3d10/ID3D10Device::GetDeviceRemovedReason, direct3d10.id3d10device_getdeviceremovedreason
ms.topic: method
f1_keywords: 
 - "d3d10/ID3D10Device.GetDeviceRemovedReason"
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GetDeviceRemovedReason
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::GetDeviceRemovedReason


## -description


Get the reason why the device was removed.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Possible return values include: 



<ul>
<li>DXGI_ERROR_DEVICE_HUNG</li>
<li>DXGI_ERROR_DEVICE_REMOVED</li>
<li>DXGI_ERROR_DEVICE_RESET</li>
<li>DXGI_ERROR_DRIVER_INTERNAL_ERROR</li>
<li>DXGI_ERROR_INVALID_CALL</li>
<li>S_OK</li>
</ul>
For more detail on these return codes, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

