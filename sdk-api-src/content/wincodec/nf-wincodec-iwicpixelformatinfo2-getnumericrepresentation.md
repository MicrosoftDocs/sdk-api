---
UID: NF:wincodec.IWICPixelFormatInfo2.GetNumericRepresentation
title: IWICPixelFormatInfo2::GetNumericRepresentation (wincodec.h)
description: Retrieves the WICPixelFormatNumericRepresentation of the pixel format.
helpviewer_keywords: ["GetNumericRepresentation","GetNumericRepresentation method [Windows Imaging Component]","GetNumericRepresentation method [Windows Imaging Component]","IWICPixelFormatInfo2 interface","IWICPixelFormatInfo2 interface [Windows Imaging Component]","GetNumericRepresentation method","IWICPixelFormatInfo2.GetNumericRepresentation","IWICPixelFormatInfo2::GetNumericRepresentation","_wic_codec_iwicpixelformatinfo2_getnumericrepresentation","wic._wic_codec_iwicpixelformatinfo2_getnumericrepresentation","wincodec/IWICPixelFormatInfo2::GetNumericRepresentation"]
old-location: wic\_wic_codec_iwicpixelformatinfo2_getnumericrepresentation.htm
tech.root: wic
ms.assetid: b987e5b9-33a4-485f-9c7a-1fcb907b5424
ms.date: 12/05/2018
ms.keywords: GetNumericRepresentation, GetNumericRepresentation method [Windows Imaging Component], GetNumericRepresentation method [Windows Imaging Component],IWICPixelFormatInfo2 interface, IWICPixelFormatInfo2 interface [Windows Imaging Component],GetNumericRepresentation method, IWICPixelFormatInfo2.GetNumericRepresentation, IWICPixelFormatInfo2::GetNumericRepresentation, _wic_codec_iwicpixelformatinfo2_getnumericrepresentation, wic._wic_codec_iwicpixelformatinfo2_getnumericrepresentation, wincodec/IWICPixelFormatInfo2::GetNumericRepresentation
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICPixelFormatInfo2::GetNumericRepresentation
 - wincodec/IWICPixelFormatInfo2::GetNumericRepresentation
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
 - IWICPixelFormatInfo2.GetNumericRepresentation
---

## -description

Retrieves the <a href="/windows/win32/api/wincodec/ne-wincodec-wicpixelformatnumericrepresentation">WICPixelFormatNumericRepresentation</a> of the pixel format.

## -parameters

### -param pNumericRepresentation [out]

Type: <b><a href="/windows/win32/api/wincodec/ne-wincodec-wicpixelformatnumericrepresentation">WICPixelFormatNumericRepresentation</a>*</b>

The address of a <a href="/windows/win32/api/wincodec/ne-wincodec-wicpixelformatnumericrepresentation">WICPixelFormatNumericRepresentation</a> variable that you've defined. On successful completion, the function sets your variable to the **WICPixelFormatNumericRepresentation** of the pixel format.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/wincodec/nn-wincodec-iwicpixelformatinfo2">IWICPixelFormatInfo2</a>

