---
UID: NF:dcomp.IDCompositionDevice2.CreateSurfaceFactory
title: IDCompositionDevice2::CreateSurfaceFactory (dcomp.h)
description: Creates a Microsoft DirectComposition surface factory object, which can be used to create other DirectComposition surface or virtual surface objects.
helpviewer_keywords: ["CreateSurfaceFactory","CreateSurfaceFactory method [DirectComposition]","CreateSurfaceFactory method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateSurfaceFactory method","IDCompositionDevice2.CreateSurfaceFactory","IDCompositionDevice2::CreateSurfaceFactory","dcomp/IDCompositionDevice2::CreateSurfaceFactory","directcomp.idcompositiondevice2_createsurfacefactory"]
old-location: directcomp\idcompositiondevice2_createsurfacefactory.htm
tech.root: directcomp
ms.assetid: 20E60EAE-68CB-45B8-BC50-3D12F449AA6E
ms.date: 12/05/2018
ms.keywords: CreateSurfaceFactory, CreateSurfaceFactory method [DirectComposition], CreateSurfaceFactory method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateSurfaceFactory method, IDCompositionDevice2.CreateSurfaceFactory, IDCompositionDevice2::CreateSurfaceFactory, dcomp/IDCompositionDevice2::CreateSurfaceFactory, directcomp.idcompositiondevice2_createsurfacefactory
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
 - IDCompositionDevice2::CreateSurfaceFactory
 - dcomp/IDCompositionDevice2::CreateSurfaceFactory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice2.CreateSurfaceFactory
---

# IDCompositionDevice2::CreateSurfaceFactory


## -description

Creates a Microsoft DirectComposition surface factory object, which can be used to create other DirectComposition surface or virtual surface objects

## -parameters

### -param renderingDevice [in]

A pointer to a DirectX device to be used to create DirectComposition surface objects. Must be a pointer to an object implementing the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> or <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> interfaces. This parameter must not be NULL.

### -param surfaceFactory [out]

The newly created surface factory object. This parameter must not be NULL.

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A surface factory allows an application to simultaneously use more than one single DXGI or Direct2D device with DirectComposition. Each surface factory has a permanent association with one DXGI or Direct2D device, but a DirectComposition device may have any number of surface factories.



Each surface factory manages resources independently from the others. In particular, DirectComposition pools surface allocations to mitigate surface allocation and deallocation costs. This pool is done on a per-surface factory basis.



If the <a href="/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice2">DCompositionCreateDevice2</a> function is called with a non-NULL <i>renderingDevice</i> parameter, the returned DirectComposition device object has an implicit surface factory under the covers associated with the given rendering device. This implicit surface factory is used to service the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createsurface">IDCompositionDevice::CreateSurface</a>, <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface">IDCompositionDevice::CreateVirtualSurface</a>, <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-createsurface">IDCompositionDevice2::CreateSurface</a> and <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-createvirtualsurface">IDCompositionDevice2::CreateVirtualSurface</a> methods.



A surface object remains alive as long as any of the surfaces or virtual surfaces that it created remain alive, either directly because the application holds a direct reference, or indirectly because one or more such surfaces are associated with one or more visual objects.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-createsurface">IDCompositionDevice2::CreateSurface</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice2-createvirtualsurface">IDCompositionDevice2::CreateVirtualSurface</a>