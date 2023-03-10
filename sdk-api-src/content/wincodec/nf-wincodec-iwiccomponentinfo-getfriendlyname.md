---
UID: NF:wincodec.IWICComponentInfo.GetFriendlyName
title: IWICComponentInfo::GetFriendlyName (wincodec.h)
description: Retrieves the component's friendly name, which is a human-readable display name for the component.
helpviewer_keywords: ["GetFriendlyName","GetFriendlyName method [Windows Imaging Component]","GetFriendlyName method [Windows Imaging Component]","IWICComponentInfo interface","IWICComponentInfo interface [Windows Imaging Component]","GetFriendlyName method","IWICComponentInfo.GetFriendlyName","IWICComponentInfo::GetFriendlyName","_wic_codec_iwiccomponentinfo_getfriendlyname","wic._wic_codec_iwiccomponentinfo_getfriendlyname","wincodec/IWICComponentInfo::GetFriendlyName"]
old-location: wic\_wic_codec_iwiccomponentinfo_getfriendlyname.htm
tech.root: wic
ms.assetid: c67e7a30-8bd5-427b-8a67-c77e3cf86e78
ms.date: 12/05/2018
ms.keywords: GetFriendlyName, GetFriendlyName method [Windows Imaging Component], GetFriendlyName method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetFriendlyName method, IWICComponentInfo.GetFriendlyName, IWICComponentInfo::GetFriendlyName, _wic_codec_iwiccomponentinfo_getfriendlyname, wic._wic_codec_iwiccomponentinfo_getfriendlyname, wincodec/IWICComponentInfo::GetFriendlyName
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
 - IWICComponentInfo::GetFriendlyName
 - wincodec/IWICComponentInfo::GetFriendlyName
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
 - IWICComponentInfo.GetFriendlyName
---

# IWICComponentInfo::GetFriendlyName


## -description

Retrieves the component's friendly name, which is a human-readable display name for the component.

## -parameters

### -param cchFriendlyName [in]

Type: <b>UINT</b>

The size of the <i>wzFriendlyName</i> buffer.

### -param wzFriendlyName [in, out]

Type: <b>WCHAR*</b>

A pointer that receives the friendly name of the component.
               The locale of the string depends on the value that the codec wrote to the registry at install time. For built-in components, these strings are always in English.

### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's friendly name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>cchFriendlyName</i> is 0 and <i>wzFriendlyName</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.

