---
UID: NF:wincodec.IWICComponentInfo.GetSpecVersion
title: IWICComponentInfo::GetSpecVersion
author: windows-driver-content
description: Retrieves the component's specification version.
old-location: wic\_wic_codec_iwiccomponentinfo_getspecversion.htm
old-project: wic
ms.assetid: 18a771c7-8764-4694-be05-29c5eda27e93
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetSpecVersion, GetSpecVersion method [Windows Imaging Component], GetSpecVersion method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetSpecVersion method, IWICComponentInfo.GetSpecVersion, IWICComponentInfo::GetSpecVersion, _wic_codec_iwiccomponentinfo_getspecversion, wic._wic_codec_iwiccomponentinfo_getspecversion, wincodec/IWICComponentInfo::GetSpecVersion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICComponentInfo.GetSpecVersion
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
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

When this method returns, contain a culture invarient string of the component's specification version. The version form is NN.NN.NN.NN.


### -param pcchActual [out]

Type: <b>UINT*</b>

A pointer that receives the actual length of the component's specification version. The specification version is optional; if a value is not specified by the component, the length returned is 0.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



All built-in components return "1.0.0.0", except for pixel formats, which do not have a spec version.

If <i>cchAuthor</i> is 0 and <i>wzAuthor</i> is <b>NULL</b>, the required buffer size is returned in <i>pccchActual</i>.



