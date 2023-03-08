---
UID: NF:wincodec.IWICBitmapCodecInfo.GetDeviceManufacturer
title: IWICBitmapCodecInfo::GetDeviceManufacturer (wincodec.h)
description: Retrieves the name of the device manufacture associated with the codec.
helpviewer_keywords: ["GetDeviceManufacturer","GetDeviceManufacturer method [Windows Imaging Component]","GetDeviceManufacturer method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","GetDeviceManufacturer method","IWICBitmapCodecInfo.GetDeviceManufacturer","IWICBitmapCodecInfo::GetDeviceManufacturer","_wic_codec_iwicbitmapcodecinfo_getdevicemanufacturer","wic._wic_codec_iwicbitmapcodecinfo_getdevicemanufacturer","wincodec/IWICBitmapCodecInfo::GetDeviceManufacturer"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_getdevicemanufacturer.htm
tech.root: wic
ms.assetid: a69e8195-5dc1-4a25-ab3c-9ea0cb3de074
ms.date: 12/05/2018
ms.keywords: GetDeviceManufacturer, GetDeviceManufacturer method [Windows Imaging Component], GetDeviceManufacturer method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],GetDeviceManufacturer method, IWICBitmapCodecInfo.GetDeviceManufacturer, IWICBitmapCodecInfo::GetDeviceManufacturer, _wic_codec_iwicbitmapcodecinfo_getdevicemanufacturer, wic._wic_codec_iwicbitmapcodecinfo_getdevicemanufacturer, wincodec/IWICBitmapCodecInfo::GetDeviceManufacturer
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
 - IWICBitmapCodecInfo::GetDeviceManufacturer
 - wincodec/IWICBitmapCodecInfo::GetDeviceManufacturer
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
 - IWICBitmapCodecInfo.GetDeviceManufacturer
---

# IWICBitmapCodecInfo::GetDeviceManufacturer


## -description

Retrieves the name of the device manufacture associated with the codec.

## -parameters

### -param cchDeviceManufacturer [in]

Type: <b>UINT</b>

The size of the device manufacture's name. Use <code>0</code> on first call to determine needed buffer size.

### -param wzDeviceManufacturer [in, out]

Type: <b>WCHAR*</b>

Receives the device manufacture's name. Use <code>NULL</code> on first call to determine needed buffer size.

### -param pcchActual [out]

Type: <b>UINT*</b>

The actual buffer size needed to retrieve the device manufacture's name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The usage pattern for this method is a two call process.
            The first call retrieves the buffer size needed to retrieve the full color management version number by calling it with <i>cchDeviceManufacturer</i> set to <code>0</code> and <i>wzDeviceManufacturer</i> set to <code>NULL</code>.
            This call sets <i>pcchActual</i> to the buffer size needed.
            Once the needed buffer size is determined, a second <b>GetDeviceManufacturer</b> call with <i>cchDeviceManufacturer</i> set to the buffer size and <i>wzDeviceManufacturer</i> set to a buffer of the appropriate size will retrieve the pixel formats.

