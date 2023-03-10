---
UID: NF:wincodec.IWICComponentInfo.GetVersion
title: IWICComponentInfo::GetVersion (wincodec.h)
description: Retrieves the component's version.
helpviewer_keywords: ["GetVersion","GetVersion method [Windows Imaging Component]","GetVersion method [Windows Imaging Component]","IWICComponentInfo interface","IWICComponentInfo interface [Windows Imaging Component]","GetVersion method","IWICComponentInfo.GetVersion","IWICComponentInfo::GetVersion","_wic_codec_iwiccomponentinfo_getversion","wic._wic_codec_iwiccomponentinfo_getversion","wincodec/IWICComponentInfo::GetVersion"]
old-location: wic\_wic_codec_iwiccomponentinfo_getversion.htm
tech.root: wic
ms.assetid: f65d13ae-ccec-49a8-8818-225464b3a117
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [Windows Imaging Component], GetVersion method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetVersion method, IWICComponentInfo.GetVersion, IWICComponentInfo::GetVersion, _wic_codec_iwiccomponentinfo_getversion, wic._wic_codec_iwiccomponentinfo_getversion, wincodec/IWICComponentInfo::GetVersion
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
 - IWICComponentInfo::GetVersion
 - wincodec/IWICComponentInfo::GetVersion
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
 - IWICComponentInfo.GetVersion
---

# IWICComponentInfo::GetVersion


## -description

Retrieves the component's version.

## -parameters

### -param cchVersion [in]

Type: <b>UINT</b>

The size of the <i>wzVersion</i> buffer.

### -param wzVersion [in, out]

Type: <b>WCHAR*</b>

A pointer that receives a culture invariant string of the component's version.

### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's version. The version is optional; if a value is not specified by the component, the length returned is 0.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

All built-in components return "1.0.0.0", except for pixel formats, which do not have a version.

If <i>cchAuthor</i> is 0 and <i>wzAuthor</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.

