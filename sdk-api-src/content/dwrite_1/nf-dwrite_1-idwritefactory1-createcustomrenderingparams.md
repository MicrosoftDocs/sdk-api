---
UID: NF:dwrite_1.IDWriteFactory1.CreateCustomRenderingParams
title: IDWriteFactory1::CreateCustomRenderingParams
author: windows-sdk-content
description: Creates a rendering parameters object with the specified properties.
old-location: directwrite\idwritefactory1_createcustomrenderingparams.htm
old-project: DirectWrite
ms.assetid: 602122A5-875E-43EC-81C8-6C3D1EEEFDAE
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateCustomRenderingParams, CreateCustomRenderingParams method [Direct Write], CreateCustomRenderingParams method [Direct Write],IDWriteFactory1 interface, IDWriteFactory1 interface [Direct Write],CreateCustomRenderingParams method, IDWriteFactory1.CreateCustomRenderingParams, IDWriteFactory1::CreateCustomRenderingParams, directwrite.idwritefactory1_createcustomrenderingparams, dwrite_1/IDWriteFactory1::CreateCustomRenderingParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory1.CreateCustomRenderingParams
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
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

Type: <b><a href="https://msdn.microsoft.com/de84b37b-bcb1-432c-8876-d84eaa0e30e0">DWRITE_PIXEL_GEOMETRY</a></b>

Represents the internal structure of a device pixel (that is, the physical arrangement of red, green, and blue color components) that is assumed for purposes of rendering text.


### -param renderingMode

Type: <b><a href="https://msdn.microsoft.com/c6b2c15a-be22-49ce-affd-1369e23f4d6b">DWRITE_RENDERING_MODE</a></b>

A value that represents the method (for example, ClearType natural quality) for rendering glyphs.


### -param renderingParams [out]

Type: <b><a href="https://msdn.microsoft.com/3A69E77A-5C22-422E-AC50-4EB9A0A472FE">IDWriteRenderingParams1</a>**</b>

When this method returns, contains an address of a pointer to the newly created rendering parameters object.


## -returns



Type: <b>HRESULT</b>

Standard HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/43FA7E32-FFAD-4F26-A225-811C2CC507DF">IDWriteFactory1</a>
 

 

