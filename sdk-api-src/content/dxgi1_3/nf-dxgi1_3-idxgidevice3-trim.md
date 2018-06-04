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

# IDXGIDevice3::Trim


## -description


Trims the graphics memory allocated by the <a href="https://msdn.microsoft.com/3D6A0173-456D-4783-943D-35F335F358BE">IDXGIDevice3</a> 
    DXGI device on the app's behalf.

For apps that render with DirectX, graphics drivers periodically allocate internal memory buffers in order to speed up subsequent rendering requests. These memory allocations count against the app's memory usage for PLM  and in general lead to increased memory usage by the overall system.

Starting in Windows 8.1, apps that render with Direct2D and/or Direct3D (including <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> and XAML interop) must call <b>Trim</b> in response to the PLM suspend callback. The Direct3D runtime and the graphics driver will discard internal memory buffers allocated for the app, reducing its memory footprint.

Calling this method does not change the rendering state of the graphics device and it has no effect on rendering operations. There is a brief performance hit when internal buffers are reallocated during the first rendering operations after the <b>Trim</b> call, therefore apps should only call <b>Trim</b> when going idle for a period of time (in response to PLM suspend, for example).

Apps should ensure that they call <b>Trim</b> as one of the last D3D operations done before going idle. Direct3D will normally defer the destruction of D3D objects. Calling <b>Trim</b>, however, forces Direct3D to destroy objects immediately. For this reason, it is not guaranteed that releasing the final reference on Direct3D objects after calling <b>Trim</b> will cause the object to be destroyed and memory to be deallocated  before the app suspends.

Similar to <a href="https://msdn.microsoft.com/e204c585-4996-4274-a654-b9912e957fe6">ID3D11DeviceContext::Flush</a>, apps should call <a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ID3D11DeviceContext::ClearState</a> before calling <b>Trim</b>. <b>ClearState</b> clears the Direct3D pipeline bindings, ensuring that Direct3D does not hold any references to the Direct3D objects you are trying to release.

It is also prudent to release references on middleware before calling <b>Trim</b>, as that middleware may also need to release references
to Direct3D objects.


## -parameters






## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/3D6A0173-456D-4783-943D-35F335F358BE">IDXGIDevice3</a>
 

 

