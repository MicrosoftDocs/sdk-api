---
UID: NF:dcomp.DCompositionCreateDevice2
title: DCompositionCreateDevice2 function (dcomp.h)
description: Creates a new device object that can be used to create other Microsoft DirectComposition objects. (DCompositionCreateDevice2)
helpviewer_keywords: ["DCompositionCreateDevice2","DCompositionCreateDevice2 function [DirectComposition]","dcomp/DCompositionCreateDevice2","directcomp.dcompositioncreatedevice2"]
old-location: directcomp\dcompositioncreatedevice2.htm
tech.root: directcomp
ms.assetid: C40694CB-7110-4ED0-B2E5-F73ADEA7BEA4
ms.date: 12/05/2018
ms.keywords: DCompositionCreateDevice2, DCompositionCreateDevice2 function [DirectComposition], dcomp/DCompositionCreateDevice2, directcomp.dcompositioncreatedevice2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCompositionCreateDevice2
 - dcomp/DCompositionCreateDevice2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dcomp.dll
 - Ext-MS-OneCore-DComp-L1-1-0.dll
api_name:
 - DCompositionCreateDevice2
---

# DCompositionCreateDevice2 function


## -description

Creates a new device object that can be used to create other Microsoft DirectComposition objects.

## -parameters

### -param renderingDevice [in, optional]

An optional pointer to a DirectX device to be used to create DirectComposition surface objects. Must be a pointer to an object implementing the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> or <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> interfaces.

### -param iid [in]

The identifier of the interface to retrieve. This must be one of __uuidof(IDCompositionDevice) or __uuidof(IDCompositionDesktopDevice).

### -param dcompositionDevice [out]

Receives an interface pointer to the newly created device object. The pointer is of the type specified by the <i>iid</i> parameter. This parameter must not be NULL.

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A device object serves as the factory for all other DirectComposition objects. It also controls transactional composition through the IDCompositionDevice2::Commit method.



The <i>renderingDevice</i> parameter may point to a <a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi">DXGI</a>, Direct3D, Direct2D device object, or it may be NULL. This parameter affects the behavior of the IDCompositionDevice2::CreateSurface, IDCompositionDevice2::CreateVirtualSurface and IDCompositionSurface::BeginDraw methods.



If the <i>renderingDevice</i> parameter is NULL then the returned DirectComposition device cannot directly create DirectComposition surface objects. In particular, IDCompositionDevice2::CreateSurface and IDCompositionDevice2::CreateVirtualSurface methods return E_INVALIDARG, regardless of the supplied parameters. However, such a DirectComposition device object can still be used to indirectly create surfaces if the application creates a surface factory object via the IDCompositionDevice2::CreateSurfaceFactory method.



If the <i>renderingDevice</i> parameter points to a DXGI device, that device is used to allocate all video memory needed by the IDCompositionDevice2::CreateSurface and IDCompositionDevice2::CreateVirtualSurface methods. Moreover, the IDCompositionSurface::BeginDraw method returns an interface pointer to a DXGI surface that belongs to that same DXGI device.



If the <i>renderingDevice</i> parameter points to a Direct2D device object, DirectComposition extracts from it the underlying DXGI device object and uses it as if that DXGI device object had been passed in as the <i>renderingDevice</i> parameter. However, passing in a Direct2D object further causes IDCompositionSurface::BeginDraw to accept __uuidof(ID2D1DeviceContext) for its <i>iid</i> parameter for any objects created with the IDCompositionDevice2::CreateSurface or IDCompositionDevice2::CreateVirtualSurface methods. In that case, the Direct2D device context object returned by IDCompositionSurface::BeginDraw will belong to the same Direct2D device passed as the <i>renderingDevice</i> parameter.



If the <i>iid</i> parameter is __uuidof(IDCompositionDevice), then the dcompositionDevice parameter receives a pointer to a Version 1 IDCompositionDevice interface, but the underlying object is a Version 2 desktop device object. The application can later obtain a pointer to either the IDCompositionDevice2 or IDCompositionDesktopDevice interfaces by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on that device. Similarly, all DirectComposition objects created from such a device are Version 2 objects under the covers. For example, the IDCompositionDevice::CreateVisual method will return an IDCompositionVisual interface to the created visual, but the application can obtain a pointer to the IDCompositionVisual2 interface via the QueryInterface method. This behavior allows an application written to the DirectComposition V1 API to incrementally adopt DirectComposition V2 features by changing the device creation method from DCompositionCreateDevice to DCompositionCreateDevice2, while still requesting the IDCompositionDevice2 interface. This allows the rest of the code to remain unchanged, while allowing the application to use QueryInterface in just the places where new functionality is needed.

## -see-also

IDCompositionDesktopDevice



IDCompositionDevice2



IDCompositionDevice2::CreateSurface



IDCompositionDevice2::CreateSurfaceFactory



IDCompositionDevice2::CreateVirtualSurface



IDCompositionSurface::BeginDraw
