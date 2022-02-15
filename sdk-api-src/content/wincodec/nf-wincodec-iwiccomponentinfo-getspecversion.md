---
UID: NF:wincodec.IWICComponentInfo.GetSpecVersion
title: IWICComponentInfo::GetSpecVersion (wincodec.h)
description: Retrieves the component's specification version.
helpviewer_keywords: ["GetSpecVersion","GetSpecVersion method [Windows Imaging Component]","GetSpecVersion method [Windows Imaging Component]","IWICComponentInfo interface","IWICComponentInfo interface [Windows Imaging Component]","GetSpecVersion method","IWICComponentInfo.GetSpecVersion","IWICComponentInfo::GetSpecVersion","_wic_codec_iwiccomponentinfo_getspecversion","wic._wic_codec_iwiccomponentinfo_getspecversion","wincodec/IWICComponentInfo::GetSpecVersion"]
old-location: wic\_wic_codec_iwiccomponentinfo_getspecversion.htm
tech.root: wic
ms.assetid: 18a771c7-8764-4694-be05-29c5eda27e93
ms.date: 12/05/2018
ms.keywords: GetSpecVersion, GetSpecVersion method [Windows Imaging Component], GetSpecVersion method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetSpecVersion method, IWICComponentInfo.GetSpecVersion, IWICComponentInfo::GetSpecVersion, _wic_codec_iwiccomponentinfo_getspecversion, wic._wic_codec_iwiccomponentinfo_getspecversion, wincodec/IWICComponentInfo::GetSpecVersion
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
 - IWICComponentInfo::GetSpecVersion
 - wincodec/IWICComponentInfo::GetSpecVersion
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
 - IWICComponentInfo.GetSpecVersion
---

# IWICComponentInfo::GetSpecVersion


## -description

Retrieves the component's specification version.

## -parameters

### -param cchSpecVersion [in]

Type: <b>UINT</b>

The size of the <i>wzSpecVersion</i> buffer.

### -param wzSpecVersion [in, out]

Type: <b>WCHAR*</b>

When this method returns, contain a culture invariant string of the component's specification version. The version form is NN.NN.NN.NN.

### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's specification version. The specification version is optional; if a value is not specified by the component, the length returned is 0.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

All built-in components return "1.0.0.0", except for pixel formats, which do not have a spec version.

If <i>cchAuthor</i> is 0 and <i>wzAuthor</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.

