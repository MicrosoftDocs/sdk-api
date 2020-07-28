---
UID: NF:wincodec.IWICColorContext.GetType
title: IWICColorContext::GetType (wincodec.h)
description: Retrieves the color context type.
helpviewer_keywords: ["GetType","GetType method [Windows Imaging Component]","GetType method [Windows Imaging Component]","IWICColorContext interface","IWICColorContext interface [Windows Imaging Component]","GetType method","IWICColorContext.GetType","IWICColorContext::GetType","_wic_codec_iwiccolorcontext_gettype","wic._wic_codec_iwiccolorcontext_gettype","wincodec/IWICColorContext::GetType"]
old-location: wic\_wic_codec_iwiccolorcontext_gettype.htm
tech.root: wic
ms.assetid: 34b23e94-bf6a-4440-825f-3997658e0095
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Windows Imaging Component], GetType method [Windows Imaging Component],IWICColorContext interface, IWICColorContext interface [Windows Imaging Component],GetType method, IWICColorContext.GetType, IWICColorContext::GetType, _wic_codec_iwiccolorcontext_gettype, wic._wic_codec_iwiccolorcontext_gettype, wincodec/IWICColorContext::GetType
f1_keywords:
- wincodec/IWICColorContext.GetType
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.lib
- Windowscodecs.dll
api_name:
- IWICColorContext.GetType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICColorContext::GetType


## -description


Retrieves the color context type.


## -parameters




### -param pType [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextType</a>*</b>

A pointer that receives the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccolorcontexttype">WICColorContextType</a> of the color context.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



