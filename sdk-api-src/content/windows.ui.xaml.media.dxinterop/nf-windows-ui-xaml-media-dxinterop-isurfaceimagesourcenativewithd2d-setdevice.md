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

# ISurfaceImageSourceNativeWithD2D::xaml


## -description


Sets the Microsoft DirectX Graphics Infrastructure (DXGI) or Direct2D device, created with <b>D3D11_CREATE_DEVICE_BGRA_SUPPORT</b>, that will draw the surface.


## -parameters




### -param device






#### - pDevice [in]

Pointer to the DXGI device interface. You can pass an <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> to signal that this surface participates in Direct2D batching to improve performance when updating Direct2D content across multiple surfaces.  The device must have multithreading supported enabled if the app draws to the surface from a background thread. 


## -returns



This method fails when the SurfaceImageSource is larger than the maximum texture size supported by the Direct3D device. Apps should use VirtualSurfaceImageSource for surfaces larger than the maximum texture size supported by the Direct3D device.




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/5C004E4F-12C6-4C2E-AE9A-D841411FF689">ISurfaceImageSourceNativeWithD2D</a>



<a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a>



<a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>
 

 

