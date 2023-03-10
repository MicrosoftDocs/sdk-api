---
UID: NF:wincodec.IWICBitmapCodecInfo.GetColorManagementVersion
title: IWICBitmapCodecInfo::GetColorManagementVersion (wincodec.h)
description: Retrieves the color management version number the codec supports.
helpviewer_keywords: ["GetColorManagementVersion","GetColorManagementVersion method [Windows Imaging Component]","GetColorManagementVersion method [Windows Imaging Component]","IWICBitmapCodecInfo interface","IWICBitmapCodecInfo interface [Windows Imaging Component]","GetColorManagementVersion method","IWICBitmapCodecInfo.GetColorManagementVersion","IWICBitmapCodecInfo::GetColorManagementVersion","_wic_codec_iwicbitmapcodecinfo_getcolormanagementversion","wic._wic_codec_iwicbitmapcodecinfo_getcolormanagementversion","wincodec/IWICBitmapCodecInfo::GetColorManagementVersion"]
old-location: wic\_wic_codec_iwicbitmapcodecinfo_getcolormanagementversion.htm
tech.root: wic
ms.assetid: 3d115306-615a-403b-95f8-3e2850928928
ms.date: 12/05/2018
ms.keywords: GetColorManagementVersion, GetColorManagementVersion method [Windows Imaging Component], GetColorManagementVersion method [Windows Imaging Component],IWICBitmapCodecInfo interface, IWICBitmapCodecInfo interface [Windows Imaging Component],GetColorManagementVersion method, IWICBitmapCodecInfo.GetColorManagementVersion, IWICBitmapCodecInfo::GetColorManagementVersion, _wic_codec_iwicbitmapcodecinfo_getcolormanagementversion, wic._wic_codec_iwicbitmapcodecinfo_getcolormanagementversion, wincodec/IWICBitmapCodecInfo::GetColorManagementVersion
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
 - IWICBitmapCodecInfo::GetColorManagementVersion
 - wincodec/IWICBitmapCodecInfo::GetColorManagementVersion
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
 - IWICBitmapCodecInfo.GetColorManagementVersion
---

# IWICBitmapCodecInfo::GetColorManagementVersion


## -description

Retrieves the color management version number the codec supports.

## -parameters

### -param cchColorManagementVersion [in]

Type: <b>UINT</b>

The size of the version buffer. Use <code>0</code> on first call to determine needed buffer size.

### -param wzColorManagementVersion [in, out]

Type: <b>WCHAR*</b>

Receives the color management version number. Use <code>NULL</code> on first call to determine needed buffer size.

### -param pcchActual [in, out]

Type: <b>UINT*</b>

The actual buffer size needed to retrieve the full color management version number.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The usage pattern for this method is a two call process.
            The first call retrieves the buffer size needed to retrieve the full color management version number by calling it with <i>cchColorManagementVersion</i> set to <code>0</code> and <i>wzColorManagementVersion</i> set to <code>NULL</code>.
            This call sets <i>pcchActual</i> to the buffer size needed.
            Once the needed buffer size is determined, a second <b>GetColorManagementVersion</b> call with <i>cchColorManagementVersion</i> set to the buffer size and <i>wzColorManagementVersion</i> set to a buffer of the appropriate size will retrieve the pixel formats.

