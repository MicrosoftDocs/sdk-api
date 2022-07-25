---
UID: NF:mfapi.MFCreateWICBitmapBuffer
title: MFCreateWICBitmapBuffer function (mfapi.h)
description: Creates a media buffer object that manages a Windows Imaging Component (WIC).
helpviewer_keywords: ["MFCreateWICBitmapBuffer","MFCreateWICBitmapBuffer function [Media Foundation]","mf.mfcreatewicbitmapbuffer","mfapi/MFCreateWICBitmapBuffer"]
old-location: mf\mfcreatewicbitmapbuffer.htm
tech.root: mf
ms.assetid: 029B7CC6-5B12-4A19-B6CD-B0D7E3F314B6
ms.date: 12/05/2018
ms.keywords: MFCreateWICBitmapBuffer, MFCreateWICBitmapBuffer function [Media Foundation], mf.mfcreatewicbitmapbuffer, mfapi/MFCreateWICBitmapBuffer
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateWICBitmapBuffer
 - mfapi/MFCreateWICBitmapBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateWICBitmapBuffer
---

# MFCreateWICBitmapBuffer function


## -description

Creates a media buffer object that manages a Windows Imaging Component (WIC) bitmap.

## -parameters

### -param riid [in]

Set this parameter to <code>__uuidof(IWICBitmap)</code>.

### -param punkSurface [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the bitmap surface. The bitmap surface must be a WIC bitmap that exposes the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> interface.

### -param ppBuffer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>