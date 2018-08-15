---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D.SetDevice
title: ISurfaceImageSourceNativeWithD2D::xaml
author: windows-sdk-content
description: Sets the Microsoft DirectX Graphics Infrastructure (DXGI) or Direct2D device, created with D3D11_CREATE_DEVICE_BGRA_SUPPORT, that will draw the surface.
old-location: winrt\isurfaceimagesourcenativewithd2d_setdevice.htm
old-project: WinRT
ms.assetid: FBBF0A5E-68FF-4143-A874-0C1100100428
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],SetDevice method, ISurfaceImageSourceNativeWithD2D.SetDevice, ISurfaceImageSourceNativeWithD2D.xaml, ISurfaceImageSourceNativeWithD2D::SetDevice, ISurfaceImageSourceNativeWithD2D::xaml, SetDevice, SetDevice method [Windows Runtime], SetDevice method [Windows Runtime],ISurfaceImageSourceNativeWithD2D interface, windows/ISurfaceImageSourceNativeWithD2D::SetDevice, winrt.isurfaceimagesourcenativewithd2d_setdevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: windows.ui.xaml.media.dxinterop.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.media.dxinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - ISurfaceImageSourceNativeWithD2D.SetDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

