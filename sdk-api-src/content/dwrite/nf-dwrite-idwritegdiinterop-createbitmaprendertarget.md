---
UID: NF:dwrite.IDWriteGdiInterop.CreateBitmapRenderTarget
title: IDWriteGdiInterop::CreateBitmapRenderTarget
author: windows-sdk-content
description: Creates an object that encapsulates a bitmap and memory DC (device context) which can be used for rendering glyphs.
old-location: directwrite\IDWriteGdiInterop_CreateBitmapRenderTarget.htm
tech.root: DirectWrite
ms.assetid: 1a1bd200-6da6-4e4d-83d3-1f6a4a5e7152
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateBitmapRenderTarget, CreateBitmapRenderTarget method [Direct Write], CreateBitmapRenderTarget method [Direct Write],IDWriteGdiInterop interface, IDWriteGdiInterop interface [Direct Write],CreateBitmapRenderTarget method, IDWriteGdiInterop.CreateBitmapRenderTarget, IDWriteGdiInterop::CreateBitmapRenderTarget, directwrite.IDWriteGdiInterop_CreateBitmapRenderTarget, dwrite/IDWriteGdiInterop::CreateBitmapRenderTarget
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
 - IDWriteGdiInterop.CreateBitmapRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteGdiInterop::CreateBitmapRenderTarget


## -description


 Creates an object that encapsulates a bitmap and memory DC (device context) which can be used for rendering glyphs.


## -parameters




### -param hdc [in, optional]

Type: <b>HDC</b>

A handle to the optional device context used to create a compatible memory DC (device context).


### -param width

Type: <b>UINT32</b>

The width of the bitmap render target.


### -param height

Type: <b>UINT32</b>

The height of the bitmap render target.


### -param renderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/9953a9e9-7772-41a3-9cd9-2340a9dd4b6f">IDWriteBitmapRenderTarget</a>**</b>

When this method returns, contains an address of a pointer to the newly created <a href="https://msdn.microsoft.com/9953a9e9-7772-41a3-9cd9-2340a9dd4b6f">IDWriteBitmapRenderTarget</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/79472021-ee12-45dd-a943-3908c9e06cde">IDWriteGdiInterop</a>
 

 

