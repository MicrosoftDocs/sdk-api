---
UID: NF:dwrite.IDWriteFactory.CreateFontFace
title: IDWriteFactory::CreateFontFace
author: windows-sdk-content
description: Creates an object that represents a font face.
old-location: directwrite\IDWriteFactory_CreateFontFace.htm
tech.root: DirectWrite
ms.assetid: bb3cd53f-a2cf-472c-aee9-88ac553f0ed0
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateFontFace method, IDWriteFactory.CreateFontFace, IDWriteFactory::CreateFontFace, directwrite.IDWriteFactory_CreateFontFace, dwrite/IDWriteFactory::CreateFontFace
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
 - IDWriteFactory.CreateFontFace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateFontFace


## -description


 Creates an object that represents a font face.


## -parameters




### -param fontFaceType

Type: <b><a href="https://msdn.microsoft.com/839527fb-2560-4472-8115-960bf5b6badd">DWRITE_FONT_FACE_TYPE</a></b>

A value that indicates the type of file format of the font face.


### -param numberOfFiles

Type: <b>UINT32</b>

The number of font files, in element count, required to represent the font face.


### -param fontFiles [in]

Type: <b>const <a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a>*</b>

A font file object representing the font face.  Because <a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>maintains its own references
     to the input font file objects, you may release them after this call.


### -param faceIndex

Type: <b>UINT32</b>

The zero-based index of a font face, in cases when the font files contain a collection of font faces.
     If the font files contain a single face, this value should be zero.


### -param fontFaceSimulationFlags

Type: <b><a href="https://msdn.microsoft.com/0881afec-2fa5-4f17-96a2-68a5293e0bba">DWRITE_FONT_SIMULATIONS</a></b>

A value that indicates which, if any, font face simulation flags for algorithmic means of making text bold or italic are applied to the current font face.


### -param fontFace [out]

Type: <b><a href="https://msdn.microsoft.com/1b6bb9e2-cf01-413c-9ee8-42bb0f703ce8">IDWriteFontFace</a>**</b>

When this method returns, contains an address of a pointer to the newly created font face object, or <b>NULL</b> in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

