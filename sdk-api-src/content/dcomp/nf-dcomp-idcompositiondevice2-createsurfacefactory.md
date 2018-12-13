---
UID: NF:dcomp.IDCompositionDevice2.CreateSurfaceFactory
title: IDCompositionDevice2::CreateSurfaceFactory
author: windows-sdk-content
description: Creates a Microsoft DirectComposition surface factory object, which can be used to create other DirectComposition surface or virtual surface objects.
old-location: directcomp\idcompositiondevice2_createsurfacefactory.htm
tech.root: directcomp
ms.assetid: 20E60EAE-68CB-45B8-BC50-3D12F449AA6E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateSurfaceFactory, CreateSurfaceFactory method [DirectComposition], CreateSurfaceFactory method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateSurfaceFactory method, IDCompositionDevice2.CreateSurfaceFactory, IDCompositionDevice2::CreateSurfaceFactory, dcomp/IDCompositionDevice2::CreateSurfaceFactory, directcomp.idcompositiondevice2_createsurfacefactory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice2.CreateSurfaceFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2::CreateSurfaceFactory


## -description


Creates a Microsoft DirectComposition surface factory object, which can be used to create other DirectComposition surface or virtual surface objects


## -parameters




### -param renderingDevice [in]

A pointer to a DirectX device to be used to create DirectComposition surface objects. Must be a pointer to an object implementing the <a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a> or <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> interfaces. This parameter must not be NULL.


### -param surfaceFactory [out]

The newly created surface factory object. This parameter must not be NULL.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A surface factory allows an application to simultaneously use more than one single DXGI or Direct2D device with DirectComposition. Each surface factory has a permanent association with one DXGI or Direct2D device, but a DirectComposition device may have any number of surface factories.



Each surface factory manages resources independently from the others. In particular, DirectComposition pools surface allocations to mitigate surface allocation and deallocation costs. This pool is done on a per-surface factory basis.



If the <a href="https://msdn.microsoft.com/en-us/library/Dn280347(v=VS.85).aspx">DCompositionCreateDevice2</a> function is called with a non-NULL <i>renderingDevice</i> parameter, the returned DirectComposition device object has an implicit surface factory under the covers associated with the given rendering device. This implicit surface factory is used to service the <a href="https://msdn.microsoft.com/en-us/library/Hh437405(v=VS.85).aspx">IDCompositionDevice::CreateSurface</a>, <a href="https://msdn.microsoft.com/en-us/library/Hh437413(v=VS.85).aspx">IDCompositionDevice::CreateVirtualSurface</a>, <a href="https://msdn.microsoft.com/en-us/library/Dn280366(v=VS.85).aspx">IDCompositionDevice2::CreateSurface</a> and <a href="https://msdn.microsoft.com/en-us/library/Dn280372(v=VS.85).aspx">IDCompositionDevice2::CreateVirtualSurface</a> methods.



A surface object remains alive as long as any of the surfaces or virtual surfaces that it created remain alive, either directly because the application holds a direct reference, or indirectly because one or more such surfaces are associated with one or more visual objects.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280354(v=VS.85).aspx">IDCompositionDevice2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn280366(v=VS.85).aspx">IDCompositionDevice2::CreateSurface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn280372(v=VS.85).aspx">IDCompositionDevice2::CreateVirtualSurface</a>
 

 

