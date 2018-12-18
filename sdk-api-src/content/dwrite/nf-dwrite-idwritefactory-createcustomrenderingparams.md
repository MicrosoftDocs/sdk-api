---
UID: NF:dwrite.IDWriteFactory.CreateCustomRenderingParams
title: IDWriteFactory::CreateCustomRenderingParams
author: windows-sdk-content
description: Creates a rendering parameters object with the specified properties.
old-location: directwrite\IDWriteFactory_CreateCustomRenderingParams.htm
tech.root: DirectWrite
ms.assetid: 1bfba2c4-755e-4bcf-82e7-610fc6b30be4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateCustomRenderingParams, CreateCustomRenderingParams method [Direct Write], CreateCustomRenderingParams method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateCustomRenderingParams method, IDWriteFactory.CreateCustomRenderingParams, IDWriteFactory::CreateCustomRenderingParams, directwrite.IDWriteFactory_CreateCustomRenderingParams, dwrite/IDWriteFactory::CreateCustomRenderingParams
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory.CreateCustomRenderingParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/de84b37b-bcb1-432c-8876-d84eaa0e30e0">DWRITE_PIXEL_GEOMETRY</a></b>

Represents the internal structure of a device pixel (that is, the physical arrangement of red, green, and blue color components) that is assumed for purposes of rendering text.


### -param renderingMode

Type: <b><a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a></b>

A value that represents the method (for example, ClearType natural quality) for rendering glyphs.


### -param renderingParams [out]

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>**</b>

When this method returns, contains an address of a pointer to the newly created rendering parameters object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

