---
UID: NF:d3d10.ID3D10Device.GetDeviceRemovedReason
title: ID3D10Device::GetDeviceRemovedReason
author: windows-sdk-content
description: Get the reason why the device was removed.
old-location: direct3d10\id3d10device_getdeviceremovedreason.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_getdeviceremovedreason.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: 0009e4c5-6ad8-a897-de23-d289a78f9671, GetDeviceRemovedReason, GetDeviceRemovedReason method [Direct3D 10], GetDeviceRemovedReason method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GetDeviceRemovedReason method, ID3D10Device.GetDeviceRemovedReason, ID3D10Device::GetDeviceRemovedReason, d3d10/ID3D10Device::GetDeviceRemovedReason, direct3d10.id3d10device_getdeviceremovedreason
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D10_USAGE
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::GetDeviceRemovedReason


## -description


Get the reason why the device was removed.


## -parameters






## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Possible return values include: 



<ul>
<li>DXGI_ERROR_DEVICE_HUNG</li>
<li>DXGI_ERROR_DEVICE_REMOVED</li>
<li>DXGI_ERROR_DEVICE_RESET</li>
<li>DXGI_ERROR_DRIVER_INTERNAL_ERROR</li>
<li>DXGI_ERROR_INVALID_CALL</li>
<li>S_OK</li>
</ul>
For more detail on these return codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

