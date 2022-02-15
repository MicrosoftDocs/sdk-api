---
UID: NF:wincodec.IWICComponentInfo.GetAuthor
title: IWICComponentInfo::GetAuthor (wincodec.h)
description: Retrieves the name of component's author.
helpviewer_keywords: ["GetAuthor","GetAuthor method [Windows Imaging Component]","GetAuthor method [Windows Imaging Component]","IWICComponentInfo interface","IWICComponentInfo interface [Windows Imaging Component]","GetAuthor method","IWICComponentInfo.GetAuthor","IWICComponentInfo::GetAuthor","_wic_codec_iwiccomponentinfo_getauthor","wic._wic_codec_iwiccomponentinfo_getauthor","wincodec/IWICComponentInfo::GetAuthor"]
old-location: wic\_wic_codec_iwiccomponentinfo_getauthor.htm
tech.root: wic
ms.assetid: c92f707f-6077-4da0-9ac4-6d1f30fb5b75
ms.date: 12/05/2018
ms.keywords: GetAuthor, GetAuthor method [Windows Imaging Component], GetAuthor method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetAuthor method, IWICComponentInfo.GetAuthor, IWICComponentInfo::GetAuthor, _wic_codec_iwiccomponentinfo_getauthor, wic._wic_codec_iwiccomponentinfo_getauthor, wincodec/IWICComponentInfo::GetAuthor
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
 - IWICComponentInfo::GetAuthor
 - wincodec/IWICComponentInfo::GetAuthor
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
 - IWICComponentInfo.GetAuthor
---

# IWICComponentInfo::GetAuthor


## -description

Retrieves the name of component's author.

## -parameters

### -param cchAuthor [in]

Type: <b>UINT</b>

The size of the <i>wzAuthor</i> buffer.

### -param wzAuthor [in, out]

Type: <b>WCHAR*</b>

A pointer that receives the name of the component's author.
               The locale of the string depends on the value that the codec wrote to the registry at install time. For built-in components, these strings are always in English.

### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's authors name. The author name is optional; if an author name is not specified by the component, the length returned is 0.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>cchAuthor</i> is 0 and <i>wzAuthor</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.

