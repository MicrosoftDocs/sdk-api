---
UID: NF:dwrite_1.IDWriteBitmapRenderTarget1.SetTextAntialiasMode
title: IDWriteBitmapRenderTarget1::SetTextAntialiasMode (dwrite_1.h)
description: Sets the current text antialiasing mode of the bitmap render target.
helpviewer_keywords: ["IDWriteBitmapRenderTarget1 interface [Direct Write]","SetTextAntialiasMode method","IDWriteBitmapRenderTarget1.SetTextAntialiasMode","IDWriteBitmapRenderTarget1::SetTextAntialiasMode","SetTextAntialiasMode","SetTextAntialiasMode method [Direct Write]","SetTextAntialiasMode method [Direct Write]","IDWriteBitmapRenderTarget1 interface","directwrite.idwritebitmaprendertarget1_settextantialiasmode","dwrite_1/IDWriteBitmapRenderTarget1::SetTextAntialiasMode"]
old-location: directwrite\idwritebitmaprendertarget1_settextantialiasmode.htm
tech.root: DirectWrite
ms.assetid: 813C984D-81BC-4CAA-8C0A-166612E8028F
ms.date: 12/05/2018
ms.keywords: IDWriteBitmapRenderTarget1 interface [Direct Write],SetTextAntialiasMode method, IDWriteBitmapRenderTarget1.SetTextAntialiasMode, IDWriteBitmapRenderTarget1::SetTextAntialiasMode, SetTextAntialiasMode, SetTextAntialiasMode method [Direct Write], SetTextAntialiasMode method [Direct Write],IDWriteBitmapRenderTarget1 interface, directwrite.idwritebitmaprendertarget1_settextantialiasmode, dwrite_1/IDWriteBitmapRenderTarget1::SetTextAntialiasMode
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
 - IDWriteBitmapRenderTarget1::SetTextAntialiasMode
 - dwrite_1/IDWriteBitmapRenderTarget1::SetTextAntialiasMode
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
 - IDWriteBitmapRenderTarget1.SetTextAntialiasMode
---

# IDWriteBitmapRenderTarget1::SetTextAntialiasMode


## -description

Sets the current text antialiasing mode of the bitmap render target.

## -parameters

### -param antialiasMode

Type: <b><a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode">DWRITE_TEXT_ANTIALIAS_MODE</a></b>

A <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode">DWRITE_TEXT_ANTIALIAS_MODE</a>-typed value that specifies the antialiasing mode.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or E_INVALIDARG if the argument is not valid.

## -remarks

The antialiasing mode of a newly-created bitmap render target defaults to 
     <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode">DWRITE_TEXT_ANTIALIAS_MODE_CLEARTYPE</a>. An app can change the antialiasing
     mode by calling <b>SetTextAntialiasMode</b>. For example, an app might specify
    <a href="/windows/win32/api/dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode">DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE</a> for grayscale antialiasing when it renders text onto a transparent bitmap.

## -see-also

<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1">IDWriteBitmapRenderTarget1</a>

