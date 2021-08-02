---
UID: NF:wincodec.IWICFormatConverterInfo.GetPixelFormats
title: IWICFormatConverterInfo::GetPixelFormats (wincodec.h)
description: Retrieves a list of GUIDs that signify which pixel formats the converter supports.
helpviewer_keywords: ["GetPixelFormats","GetPixelFormats method [Windows Imaging Component]","GetPixelFormats method [Windows Imaging Component]","IWICFormatConverterInfo interface","IWICFormatConverterInfo interface [Windows Imaging Component]","GetPixelFormats method","IWICFormatConverterInfo.GetPixelFormats","IWICFormatConverterInfo::GetPixelFormats","_wic_codec_iwicformatconverterinfo_getpixelformats","wic._wic_codec_iwicformatconverterinfo_getpixelformats","wincodec/IWICFormatConverterInfo::GetPixelFormats"]
old-location: wic\_wic_codec_iwicformatconverterinfo_getpixelformats.htm
tech.root: wic
ms.assetid: 3ac86012-cf1a-47b5-b48f-7e4e94ed9805
ms.date: 12/05/2018
ms.keywords: GetPixelFormats, GetPixelFormats method [Windows Imaging Component], GetPixelFormats method [Windows Imaging Component],IWICFormatConverterInfo interface, IWICFormatConverterInfo interface [Windows Imaging Component],GetPixelFormats method, IWICFormatConverterInfo.GetPixelFormats, IWICFormatConverterInfo::GetPixelFormats, _wic_codec_iwicformatconverterinfo_getpixelformats, wic._wic_codec_iwicformatconverterinfo_getpixelformats, wincodec/IWICFormatConverterInfo::GetPixelFormats
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
 - IWICFormatConverterInfo::GetPixelFormats
 - wincodec/IWICFormatConverterInfo::GetPixelFormats
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
 - IWICFormatConverterInfo.GetPixelFormats
---

# IWICFormatConverterInfo::GetPixelFormats


## -description

Retrieves a list of GUIDs that signify which pixel formats the converter supports.

## -parameters

### -param cFormats [in]

Type: <b>UINT</b>

The size of the <i>pPixelFormatGUIDs</i> array.

### -param pPixelFormatGUIDs [in, out]

Type: <b>WICPixelFormatGUID*</b>

Pointer to a GUID array that receives the pixel formats the converter supports.

### -param pcActual [out]

Type: <b>UINT*</b>

The actual array size needed to retrieve all pixel formats supported by the converter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The format converter does not necessarily guarantee symmetricality with respect to conversion; that is, a converter may be able to convert FROM a particular format without actually being able to convert TO a particular format. In order to test symmetricality, use <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicformatconverter-canconvert">CanConvert</a>.

To determine the number of pixel formats a converter can handle, set <i>cFormats</i> to <code>0</code> and <i>pPixelFormatGUIDs</i> to <code>NULL</code>. The converter will fill <i>pcActual</i> with the number of formats supported by that converter.