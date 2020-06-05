---
UID: NF:wincodec.IWICDevelopRaw.SetNamedWhitePoint
title: IWICDevelopRaw::SetNamedWhitePoint (wincodec.h)
description: Sets the named white point of the raw file.helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetNamedWhitePoint method","IWICDevelopRaw.SetNamedWhitePoint","IWICDevelopRaw::SetNamedWhitePoint","SetNamedWhitePoint","SetNamedWhitePoint method [Windows Imaging Component]","SetNamedWhitePoint method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_setnamedwhitepoint","wic._wic_codec_iwicdevelopraw_setnamedwhitepoint","wincodec/IWICDevelopRaw::SetNamedWhitePoint"]
old-location: wic\_wic_codec_iwicdevelopraw_setnamedwhitepoint.htm
tech.root: wic
ms.assetid: eb83233d-7967-4160-bebf-2b06378f77ab
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetNamedWhitePoint method, IWICDevelopRaw.SetNamedWhitePoint, IWICDevelopRaw::SetNamedWhitePoint, SetNamedWhitePoint, SetNamedWhitePoint method [Windows Imaging Component], SetNamedWhitePoint method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_setnamedwhitepoint, wic._wic_codec_iwicdevelopraw_setnamedwhitepoint, wincodec/IWICDevelopRaw::SetNamedWhitePoint
f1_keywords:
- wincodec/IWICDevelopRaw.SetNamedWhitePoint
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.dll
api_name:
- IWICDevelopRaw.SetNamedWhitePoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICDevelopRaw::SetNamedWhitePoint


## -description


Sets the named white point of the raw file.


## -parameters




### -param WhitePoint [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wicnamedwhitepoint">WICNamedWhitePoint</a></b>

A bitwise combination of the enumeration values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the named white points are not supported by the raw image or the raw file contains named white points that are not supported by this API, the codec implementer should still mark this capability as supported.

If the named white points are not supported by the raw image, a best effort should be made to adjust the image to the named white point even when it isn't a pre-defined white point of the raw file.

If the raw file containes named white points not supported by this API, the codec implementer should support the named white points in the API.

Due to other white point setting methods (e.g. <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicdevelopraw-setwhitepointkelvin">SetWhitePointKelvin</a>), care must be taken by codec implementers to ensure proper interoperability. For instance, if the caller sets via a named white point then the codec implementer may whis to disable reading back the correspoinding Kelvin temperature. In specific cases where the codec implementer wishes to deny a given action because of previous calls, <b>WINCODEC_ERR_WRONGSTATE</b> should be returned.



