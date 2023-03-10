---
UID: NN:wincodec.IWICColorContext
title: IWICColorContext (wincodec.h)
description: Exposes methods for color management.
helpviewer_keywords: ["IWICColorContext","IWICColorContext interface [Windows Imaging Component]","IWICColorContext interface [Windows Imaging Component]","described","_wic_codec_iwiccolorcontext","wic._wic_codec_iwiccolorcontext","wincodec/IWICColorContext"]
old-location: wic\_wic_codec_iwiccolorcontext.htm
tech.root: wic
ms.assetid: b6817676-affb-4bb3-adba-e24e0b75ad10
ms.date: 12/05/2018
ms.keywords: IWICColorContext, IWICColorContext interface [Windows Imaging Component], IWICColorContext interface [Windows Imaging Component],described, _wic_codec_iwiccolorcontext, wic._wic_codec_iwiccolorcontext, wincodec/IWICColorContext
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
 - IWICColorContext
 - wincodec/IWICColorContext
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
 - IWICColorContext
---

# IWICColorContext interface


## -description

Exposes methods for color management.

## -inheritance

The <b>IWICColorContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICColorContext</b> also has these types of members:

## -remarks

A Color Context is an abstraction for a color profile. The profile can either be loaded from a file (like "sRGB Color Space Profile.icm"), read from a memory buffer, or can be defined by an EXIF color space. The system color profile directory can be obtained by calling [GetColorDirectoryW](/windows/win32/api/icm/nf-icm-getcolordirectoryw).

Once a color context has been initialized, it cannot be re-initialized.
