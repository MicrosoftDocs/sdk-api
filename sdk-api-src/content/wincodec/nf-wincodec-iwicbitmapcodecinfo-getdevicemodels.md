---
UID: NF:wincodec.IWICBitmapCodecInfo.GetDeviceModels
title: IWICBitmapCodecInfo::GetDeviceModels (wincodec.h)
description: Retrieves a comma delimited list of device models associated with the codec.
helpviewer_keywords: ["GetDeviceModels","GetDeviceModels method [Windows Imaging Component]","GetDeviceModels method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","GetDeviceModels method","IWICBitmapCodecInfo.GetDeviceModels","IWICBitmapCodecInfo::GetDeviceModels","_wic_codec_iwicbitmapcodecinfo_getdevicemodels","wic._wic_codec_iwicbitmapcodecinfo_getdevicemodels","wincodec/IWICBitmapCodecInfo::GetDeviceModels"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_getdevicemodels.htm
tech.root: wic
ms.assetid: ccc5aab6-8817-4c18-8e52-a1372b015541
ms.date: 12/05/2018
ms.keywords: GetDeviceModels, GetDeviceModels method [Windows Imaging Component], GetDeviceModels method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],GetDeviceModels method, IWICBitmapCodecInfo.GetDeviceModels, IWICBitmapCodecInfo::GetDeviceModels, _wic_codec_iwicbitmapcodecinfo_getdevicemodels, wic._wic_codec_iwicbitmapcodecinfo_getdevicemodels, wincodec/IWICBitmapCodecInfo::GetDeviceModels
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
 - IWICBitmapCodecInfo::GetDeviceModels
 - wincodec/IWICBitmapCodecInfo::GetDeviceModels
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
 - IWICBitmapCodecInfo.GetDeviceModels
---

# IWICBitmapCodecInfo::GetDeviceModels


## -description

Retrieves a comma delimited list of device models associated with the codec.

## -parameters

### -param cchDeviceModels [in]

Type: <b>UINT</b>

The size of the device models buffer. Use <code>0</code> on first call to determine needed buffer size.

### -param wzDeviceModels [in, out]

Type: <b>WCHAR*</b>

Receives a comma delimited list of device model names associated with the codec. Use <code>NULL</code> on first call to determine needed buffer size.

### -param pcchActual [in, out]

Type: <b>UINT*</b>

The actual buffer size needed to retrieve all of the device model names.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The usage pattern for this method is a two call process.
            The first call retrieves the buffer size needed to retrieve the full color management version number by calling it with <i>cchDeviceModels</i> set to <code>0</code> and <i>wzDeviceModels</i> set to <code>NULL</code>.
            This call sets <i>pcchActual</i> to the buffer size needed.
            Once the needed buffer size is determined, a second <b>GetDeviceModels</b> call with <i>cchDeviceModels</i> set to the buffer size and <i>wzDeviceModels</i> set to a buffer of the appropriate size will retrieve the pixel formats.

