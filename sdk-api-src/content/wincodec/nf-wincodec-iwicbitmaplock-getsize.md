---
UID: NF:wincodec.IWICBitmapLock.GetSize
title: IWICBitmapLock::GetSize (wincodec.h)
description: Retrieves the width and height, in pixels, of the locked rectangle.
helpviewer_keywords: ["GetSize","GetSize method [Windows Imaging Component]","GetSize method [Windows Imaging Component]","IWICBitmapLock interface","IWICBitmapLock interface [Windows Imaging Component]","GetSize method","IWICBitmapLock.GetSize","IWICBitmapLock::GetSize","_wic_codec_iwicbitmaplock_getsize","wic._wic_codec_iwicbitmaplock_getsize","wincodec/IWICBitmapLock::GetSize"]
old-location: wic\_wic_codec_iwicbitmaplock_getsize.htm
tech.root: wic
ms.assetid: 355e81ec-d08a-464e-9b4e-fa8828e30406
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [Windows Imaging Component], GetSize method [Windows Imaging Component],IWICBitmapLock interface, IWICBitmapLock interface [Windows Imaging Component],GetSize method, IWICBitmapLock.GetSize, IWICBitmapLock::GetSize, _wic_codec_iwicbitmaplock_getsize, wic._wic_codec_iwicbitmaplock_getsize, wincodec/IWICBitmapLock::GetSize
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapLock::GetSize
 - wincodec/IWICBitmapLock::GetSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapLock.GetSize
---

# IWICBitmapLock::GetSize


## -description

Retrieves the width and height, in pixels, of the locked rectangle.

## -parameters

### -param puiWidth [in, out]

Type: <b>UINT*</b>

A pointer that receives the width of the locked rectangle.

### -param puiHeight [in, out]

Type: <b>UINT*</b>

A pointer that receives the height of the locked rectangle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

