---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceManagerNative.FlushAllSurfacesWithDevice
title: ISurfaceImageSourceManagerNative::xaml
author: windows-sdk-content
description: Flushes all current GPU work for all SurfaceImageSource or VirtualSurfaceImageSource objects associated with the given device.
old-location: winrt\isurfaceimagesourcemanagernative_flushallsurfaceswithdevice.htm
tech.root: WinRT
ms.assetid: 2921FF9E-25C5-4DF6-B23F-7B60F0577983
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FlushAllSurfacesWithDevice, FlushAllSurfacesWithDevice method [Windows Runtime], FlushAllSurfacesWithDevice method [Windows Runtime],ISurfaceImageSourceManagerNative interface, ISurfaceImageSourceManagerNative interface [Windows Runtime],FlushAllSurfacesWithDevice method, ISurfaceImageSourceManagerNative.FlushAllSurfacesWithDevice, ISurfaceImageSourceManagerNative.xaml, ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice, ISurfaceImageSourceManagerNative::xaml, windows/ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice, winrt.isurfaceimagesourcemanagernative_flushallsurfaceswithdevice
ms.topic: method
req.header: windows.ui.xaml.media.dxinterop.h
req.include-header: 
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
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - ISurfaceImageSourceManagerNative.FlushAllSurfacesWithDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISurfaceImageSourceManagerNative::xaml


## -description


Flushes all current GPU work for all <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> or <a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>  objects associated with the given device.


## -parameters




### -param device [in]

The device that was used to create <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> objects in this process.  It must be an <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> or an <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>FlushAllSurfacesWithDevice</b> method flushes current GPU work for all <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> objects that were created with <i>device</i>.  This GPU work includes Direct2D rendering work and internal GPU work done by the framework associated with rendering.  This is useful if an application has created multiple <b>SurfaceImageSource</b> objects and needs to flush the GPU work for all of these surfaces from the background rendering thread.  By flushing this work from the background thread the work can be better parallelized, with work being done on the UI thread to improve performance.

You can call the <b>FlushAllSurfacesWithDevice</b> method from a non-UI thread.  




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>



<a href="https://msdn.microsoft.com/6DFC7A3D-0C29-421B-ADB0-360017DE7433">ISurfaceImageSourceManagerNative</a>



<a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a>



<a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>
 

 

