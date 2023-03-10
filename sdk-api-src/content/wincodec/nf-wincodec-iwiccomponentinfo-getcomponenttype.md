---
UID: NF:wincodec.IWICComponentInfo.GetComponentType
title: IWICComponentInfo::GetComponentType (wincodec.h)
description: Retrieves the component's WICComponentType.
helpviewer_keywords: ["GetComponentType","GetComponentType method [Windows Imaging Component]","GetComponentType method [Windows Imaging Component]","IWICComponentInfo interface","IWICComponentInfo interface [Windows Imaging Component]","GetComponentType method","IWICComponentInfo.GetComponentType","IWICComponentInfo::GetComponentType","_wic_codec_iwiccomponentinfo_getcomponenttype","wic._wic_codec_iwiccomponentinfo_getcomponenttype","wincodec/IWICComponentInfo::GetComponentType"]
old-location: wic\_wic_codec_iwiccomponentinfo_getcomponenttype.htm
tech.root: wic
ms.assetid: e7599299-2854-4796-8760-740a6ae7ad4f
ms.date: 12/05/2018
ms.keywords: GetComponentType, GetComponentType method [Windows Imaging Component], GetComponentType method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetComponentType method, IWICComponentInfo.GetComponentType, IWICComponentInfo::GetComponentType, _wic_codec_iwiccomponentinfo_getcomponenttype, wic._wic_codec_iwiccomponentinfo_getcomponenttype, wincodec/IWICComponentInfo::GetComponentType
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
 - IWICComponentInfo::GetComponentType
 - wincodec/IWICComponentInfo::GetComponentType
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
 - IWICComponentInfo.GetComponentType
---

# IWICComponentInfo::GetComponentType


## -description

Retrieves the component's <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccomponenttype">WICComponentType</a>.

## -parameters

### -param pType [out]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wiccomponenttype">WICComponentType</a>*</b>

A pointer that receives the <a href="/windows/desktop/api/wincodec/ne-wincodec-wiccomponenttype">WICComponentType</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.