---
UID: NF:dwrite_1.IDWriteFactory1.CreateCustomRenderingParams
title: IDWriteFactory1::CreateCustomRenderingParams (dwrite_1.h)
description: Creates a rendering parameters object with the specified properties. (IDWriteFactory1.CreateCustomRenderingParams)
helpviewer_keywords: ["CreateCustomRenderingParams","CreateCustomRenderingParams method [Direct Write]","CreateCustomRenderingParams method [Direct Write]","IDWriteFactory1 interface","IDWriteFactory1 interface [Direct Write]","CreateCustomRenderingParams method","IDWriteFactory1.CreateCustomRenderingParams","IDWriteFactory1::CreateCustomRenderingParams","directwrite.idwritefactory1_createcustomrenderingparams","dwrite_1/IDWriteFactory1::CreateCustomRenderingParams"]
old-location: directwrite\idwritefactory1_createcustomrenderingparams.htm
tech.root: DirectWrite
ms.assetid: 602122A5-875E-43EC-81C8-6C3D1EEEFDAE
ms.date: 12/05/2018
ms.keywords: CreateCustomRenderingParams, CreateCustomRenderingParams method [Direct Write], CreateCustomRenderingParams method [Direct Write],IDWriteFactory1 interface, IDWriteFactory1 interface [Direct Write],CreateCustomRenderingParams method, IDWriteFactory1.CreateCustomRenderingParams, IDWriteFactory1::CreateCustomRenderingParams, directwrite.idwritefactory1_createcustomrenderingparams, dwrite_1/IDWriteFactory1::CreateCustomRenderingParams
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteFactory1::CreateCustomRenderingParams
 - dwrite_1/IDWriteFactory1::CreateCustomRenderingParams
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
 - IDWriteFactory1.CreateCustomRenderingParams
---

# IDWriteFactory1::CreateCustomRenderingParams


## -description

Creates a rendering parameters object with the specified properties.

## -parameters

### -param gamma

Type: <b>FLOAT</b>

The gamma level to be set for the new rendering parameters object.

### -param enhancedContrast

Type: <b>FLOAT</b>

The enhanced contrast level to be set for the new rendering parameters object.

### -param enhancedContrastGrayscale

Type: <b>FLOAT</b>

The amount of contrast enhancement to use for grayscale antialiasing, zero or greater.

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

Type: <b><a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1">IDWriteRenderingParams1</a>**</b>

When this method returns, contains an address of a pointer to the newly created rendering parameters object.

## -returns

Type: <b>HRESULT</b>

Standard HRESULT error code.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1">IDWriteFactory1</a>

