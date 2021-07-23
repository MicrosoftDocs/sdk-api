---
UID: NF:dcomp.DCompositionCreateDevice3
title: DCompositionCreateDevice3 function (dcomp.h)
description: Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.
helpviewer_keywords: ["DCompositionCreateDevice3","DCompositionCreateDevice3 function [DirectComposition]","dcomp/DCompositionCreateDevice3","directcomp.dcompositioncreatedevice3"]
old-location: directcomp\dcompositioncreatedevice3.htm
tech.root: directcomp
ms.assetid: 5EF8F6E9-7632-42B4-A589-10CD4ABC7695
ms.date: 12/05/2018
ms.keywords: DCompositionCreateDevice3, DCompositionCreateDevice3 function [DirectComposition], dcomp/DCompositionCreateDevice3, directcomp.dcompositioncreatedevice3
req.header: dcomp.h
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCompositionCreateDevice3
 - dcomp/DCompositionCreateDevice3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dcomp.dll
api_name:
 - DCompositionCreateDevice3
---

# DCompositionCreateDevice3 function


## -description

Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.

## -parameters

### -param renderingDevice [in, optional]

Type: <b>IUnknown*</b>

An optional pointer to a DirectX device to be used to create DirectComposition surface objects. Must be a pointer to an object implementing the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> or <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> interfaces.

### -param iid [in]

Type: <b>REFIID</b>

The identifier of the interface to retrieve. This must be one of __uuidof(IDCompositionDevice) or __uuidof(IDCompositionDesktopDevice).

### -param dcompositionDevice [out]

Type: <b>void**</b>

Receives an interface pointer to the newly created device object. The pointer is of the type specified by the <i>iid</i> parameter. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.