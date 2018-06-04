---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D11_MAP_FLAG enumeration


## -description


Specifies how the CPU should respond when an application calls the <a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">ID3D11DeviceContext::Map</a> method on a resource that is being used by the GPU.


## -enum-fields




### -field D3D11_MAP_FLAG_DO_NOT_WAIT

Specifies that <a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">ID3D11DeviceContext::Map</a> should return DXGI_ERROR_WAS_STILL_DRAWING when the GPU blocks the CPU from accessing a resource. For more information about this error code, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.


## -remarks



This enumeration is used by <a href="https://msdn.microsoft.com/c9d57873-1faa-42fa-855c-26f565e3b27c">ID3D11DeviceContext::Map</a>.

D3D11_MAP_FLAG_DO_NOT_WAIT cannot be used with <a href="https://msdn.microsoft.com/916b00bd-2711-4ebd-a36d-d75b3a59a528">D3D11_MAP_WRITE_DISCARD</a> or <a href="https://msdn.microsoft.com/916b00bd-2711-4ebd-a36d-d75b3a59a528">D3D11_MAP_WRITE_NOOVERWRITE</a>.




## -see-also




<a href="https://msdn.microsoft.com/b547819b-7006-40b5-84a4-adf198048051">Resource Enumerations</a>
 

 

