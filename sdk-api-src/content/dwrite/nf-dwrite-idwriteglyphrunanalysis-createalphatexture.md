---
UID: NF:dwrite.IDWriteGlyphRunAnalysis.CreateAlphaTexture
title: IDWriteGlyphRunAnalysis::CreateAlphaTexture
author: windows-sdk-content
description: Creates an alpha texture of the specified type for glyphs within a specified bounding rectangle.
old-location: directwrite\IDWriteGlyphRunAnalysis_CreateAlphaTexture.htm
tech.root: DirectWrite
ms.assetid: a3a28efa-b235-4608-8410-15cc0ebfe38e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateAlphaTexture, CreateAlphaTexture method [Direct Write], CreateAlphaTexture method [Direct Write],IDWriteGlyphRunAnalysis interface, IDWriteGlyphRunAnalysis interface [Direct Write],CreateAlphaTexture method, IDWriteGlyphRunAnalysis.CreateAlphaTexture, IDWriteGlyphRunAnalysis::CreateAlphaTexture, directwrite.IDWriteGlyphRunAnalysis_CreateAlphaTexture, dwrite/IDWriteGlyphRunAnalysis::CreateAlphaTexture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteGlyphRunAnalysis.CreateAlphaTexture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteGlyphRunAnalysis::CreateAlphaTexture


## -description


 Creates an alpha texture of the specified type for glyphs within a specified bounding rectangle.


## -parameters




### -param textureType

Type: <b><a href="https://msdn.microsoft.com/c97ee0fd-2743-4f72-aa69-bf5e3780aa33">DWRITE_TEXTURE_TYPE</a></b>

A value that specifies the type of texture requested. This can be <a href="https://msdn.microsoft.com/c97ee0fd-2743-4f72-aa69-bf5e3780aa33">DWRITE_TEXTURE_BILEVEL_1x1</a> or <b>DWRITE_TEXTURE_CLEARTYPE_3x1</b>. If a bi-level texture is requested, the
     texture contains only bi-level glyphs. Otherwise, the texture contains only antialiased glyphs.


### -param textureBounds [in]

Type: <b>const RECT*</b>

The bounding rectangle of the texture, which can be different than
     the bounding rectangle returned by <a href="https://msdn.microsoft.com/9058edb7-23b2-418a-abcc-3ee827a79144">GetAlphaTextureBounds</a>.


### -param alphaValues [out]

Type: <b>BYTE*</b>

When this method returns, contains  the array of alpha values from the texture. The buffer allocated for this array must be at least the size of <i>bufferSize</i>.


### -param bufferSize

Type: <b>UINT32</b>

The size of the <i>alphaValues</i> array, in bytes. The minimum size depends on the dimensions of the
     rectangle and the type of texture requested.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d4739b55-1a9b-4346-9b47-d8adb98df163">IDWriteGlyphRunAnalysis</a>
 

 

