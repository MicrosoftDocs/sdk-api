---
UID: NF:dwrite.IDWriteFactory.CreateCustomRenderingParams
title: IDWriteFactory::CreateCustomRenderingParams (dwrite.h)
description: Creates a rendering parameters object with the specified properties. (IDWriteFactory.CreateCustomRenderingParams)
helpviewer_keywords: ["CreateCustomRenderingParams","CreateCustomRenderingParams method [Direct Write]","CreateCustomRenderingParams method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateCustomRenderingParams method","IDWriteFactory.CreateCustomRenderingParams","IDWriteFactory::CreateCustomRenderingParams","directwrite.IDWriteFactory_CreateCustomRenderingParams","dwrite/IDWriteFactory::CreateCustomRenderingParams"]
old-location: directwrite\IDWriteFactory_CreateCustomRenderingParams.htm
tech.root: DirectWrite
ms.assetid: 1bfba2c4-755e-4bcf-82e7-610fc6b30be4
ms.date: 12/05/2018
ms.keywords: CreateCustomRenderingParams, CreateCustomRenderingParams method [Direct Write], CreateCustomRenderingParams method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateCustomRenderingParams method, IDWriteFactory.CreateCustomRenderingParams, IDWriteFactory::CreateCustomRenderingParams, directwrite.IDWriteFactory_CreateCustomRenderingParams, dwrite/IDWriteFactory::CreateCustomRenderingParams
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFactory::CreateCustomRenderingParams
 - dwrite/IDWriteFactory::CreateCustomRenderingParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory.CreateCustomRenderingParams
---

# IDWriteFactory::CreateCustomRenderingParams


## -description

Creates a rendering parameters object with the specified properties.

## -parameters

### -param gamma

Type: <b>FLOAT</b>

The gamma level to be set for the new rendering parameters object.

### -param enhancedContrast

Type: <b>FLOAT</b>

The enhanced contrast level to be set for the new rendering parameters object.

### -param clearTypeLevel

Type: <b>FLOAT</b>

The ClearType level to be set for the new rendering parameters object.

### -param pixelGeometry

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry">DWRITE_PIXEL_GEOMETRY</a></b>

Represents the internal structure of a device pixel (that is, the physical arrangement of red, green, and blue color components) that is assumed for purposes of rendering text.

### -param renderingMode

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode">DWRITE_RENDERING_MODE</a></b>

A value that represents the method (for example, ClearType natural quality) for rendering glyphs.

### -param renderingParams [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>**</b>

When this method returns, contains an address of a pointer to the newly created rendering parameters object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

